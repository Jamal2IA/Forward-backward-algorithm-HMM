 <a name="readme-top"></a>
 
  
<br />
<div align="center">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  <h3 align="center">Forward Backward algorithm</h3> 
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#set-up">Set up</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
 

Hidden Markov Model is a Markov Chain which is mainly used in problems with temporal sequence of data. Markov Model explains that the next step depends only on the previous step in a temporal sequence. In Hidden Markov Model the state of the system is hidden (invisible), however each state emits a symbol at every time step.



As we have discussed earlier, Hidden Markov Model $(\theta)$ has with following parameters:
- Set of M Hidden States $\left(S^M\right)$
- A Transaction Probability Matrix (A)
- A sequence of $T$ observations $\left(V^T\right)$
- A Emission Probability Matrix (Also known as Observation Likelihood) (B)
- An Initial Probability Distribution $(\pi)$
In case you are not sure of any of above terminology, please refer my previous article on Introduction to Hidden Markov Model:

Forward-backward pseudo-code :


    input: guessState
           int sequenceIndex
    output: result
    if sequenceIndex is past the end of the sequence then
        return 1
    if (guessState, sequenceIndex) has been seen before then
        return saved result

    result := 0

    for each neighboring state n:
        result := result + (transition probability from guessState to 
                            n given observation element at sequenceIndex)
                            × Backward(n, sequenceIndex + 1)

    save result for (guessState, sequenceIndex)

    return result

 

 
 



<!-- Set up-->
 ## Set up

To set up this project locally follow these steps
 
### Installation

 
1. Clone the repo
   ```sh
   git clone https://github.com/Jamal2IA/Forward-backward-algorithm-HMM.git
   ```
3. create a new virtual environment ( if you want to work with your main environment skip step 2  and 3 )
   ```sh
   conda create -n forwardbackward
   ```
4. Add it as a kernel 
   ```sh
   conda install -c anaconda ipykernel
   ```
   ```sh
   python -m ipykernel install --user --name=forwardbackward
   ```
5. Install numpy
   ```sh
   pip install numpy
   ```
6. Install pandas
   ```sh
   pip install pandas
   ```
<p align="right">(<a href="#readme-top">back to top</a>)</p>



 

<!-- CONTACT -->
## Contact

Jamal Rebii- [JamalAI](https://jamal-ai.vercel.app/) - rebiijamal1@gmail.com

Project Link: [https://github.com/Jamal2IA/Forward-backward-algorithm-HMM](https://github.com/Jamal2IA/Forward-backward-algorithm-HMM)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

 
 

 
