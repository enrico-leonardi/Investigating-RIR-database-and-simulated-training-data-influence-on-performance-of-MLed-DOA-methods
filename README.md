## Investigating the influence of RIR database and simulated training data on the performance of machine learned DOA methods

## Project Contributers
<ul>
  <li>Enrico Leonardi (student - 222721)</li>
  <li>Rasmus Kongsgaard Olsson (supervisor - Principal Research Scientist - GN Audio)</li>
  <li>Cheol-Ho Jeong (supervisor - Associate Professor - DTU Electro)</li>
</ul>

## Abstract:
Direction of Arrival (DoA) estimation, also known as Sound Source Localization (SSL), is a well­-known challenge in the acoustics community. This study utilizes simulated speech recordings obtained from two different databases of Room Impulse Responses (RIRs) representing various virtual spaces. The first database is based on the Image-Source Method, a Geometrical Acoustic (GA) algorithm, while the second employs a hybrid method combining Wave­Based (WB) methods for lower frequencies and GA methods for higher frequencies. GA methods are a class of algorithms where the acoustic wave is approximated as a bundle of rays propagated in the room following the laws of ray optics, whereas WB methods directly approximate solutions of the partial differential equations governing wave motion. Being the training data based on such simulations, to address DoA estimation we utilize a Deep Neural Network (DoANet), performing iterative per­-audio frame classification across possible DoAs within the azimuthal space of [−90, 90] degrees. Several preprocessing steps for the simulated training data will be compared by evaluating DoANet’s performance on real­world recordings. These preprocessing steps, representing the project’s experiments, involve signal processing, data selection, and data manipulation. The effects of these steps will be assessed and discussed based on the network’s output.<br/><br/> My work aimed to better understand which parameters are most and least relevant in DoA estimation using mentioned machine learned methods. Additionally, I provide a comprehensive overview of acoustic simulation methods, machine learning techniques, and preprocessing steps. This project is a joint collaboration between _GN_ and _DTU_, developed primarily at the company’s facilities.

## Data
Many of the scripts used (e.g. _Matlab_ scripts to compute the simulated recordings, or _Python_ scripts to train the NN and apply it to real data) were provided by _GN_. My contributions primarily involved adjusting the provided base scripts/tools to my framework, designing and implementing the experiments, and showcasing/discussing the results. Due to the signed non­-disclosure agreement with the company, no specific lines of code has been attached to this thesis.

## Goal
This study aims to use a Convolutional Neural Network (CNN) to compute the DoA of simulated recordings, expressed as azimuthal angle estimation. The simulated data is derived from anechoic recordings and large databases of two main types of provided RIRs: one developed solely by _GN_, and the other produced through a joint project between GN and the Icelandic company _Treble Technologies_. The research seeks to identify the most relevant data parameters for the DoA problem by considering the differences in simulation methods, and consequently refining the training data so that the CNN can achieve a desired performance over real-­world scenarios.

## Usage
Being no specific lines of code attached, the purpose of this repository is not to replicate my project but rather to showcase its outcomes. For a detailed description of my work, please refer to the document _DTU GN Master Thesis Enrico Leonardi.pdf_.

## Conclusion
Sound Source Localization (SSL) is the problem of estimating the position of one or several sound sources relative to the position of the recording microphone array, based on a recorded multichannel acoustic signals. Traditional SSL approaches rely on signal processing techniques, which, despite their historical advancements, often falter in complex real-world scenarios characterized by noise, reverberation, and multiple simultaneous sound sources. Over the past decade, the emergence of data­driven DL methods has garnered significant attention for tackling these challenging circumstances. This study, simplifying the SSL problem to estimating the DoA of the sources within the azimuthal plane, aims to employ a CNN to compute the DoA of simulated recordings.<br /> <br /> Large databases of RIRs and anechoic recordings have provided the basis for generating simulated recordings. The project’s objective was to train a CNN using these simulated recordings to enable it to estimate DoA in real-­world scenarios. Two distinct simulation methods were employed to generate the training data. Numerous experiments were conducted and analyzed, focusing on identifying the most critical components of the simulated data to address the DoA problem. Key findings include:
<ul>
  <li>The CNN’s performance with Short-Time-Fourier-Transformed input recordings was initially assessed, demonstrating the feasibility of addressing the DoA problem with this setup. This served as a baseline for comparing subsequent experiments;</li>
  <li>Filtering operations were applied to the training data, revealing that low frequencies in simulated recordings alone were sufficient for effective DoA estimation, often more significant than high frequencies;</li>
  <li>A time domain experiment was conducted to validate the CNN’s architecture for the DoA task;</li>
  <li>Halving the number of microphones in the array showed that not only using fewer (than 8) microphones may suffice for the task, but also highlighted potential improvements in receiver simulation methods;</li>
  <li>An experiment in the Mel-­frequency domain reaffirmed the findings of earlier experiments, marking a foundation for future project developments in this domain.</li>
</ul>
These experiments and discussions have provided valuable insights and potential directions for future research in the field. Deep learning has demonstrated its effectiveness in tackling the DoA problem, suggesting further promising advancements ahead.
