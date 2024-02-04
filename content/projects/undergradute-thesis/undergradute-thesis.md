---
title: "Quantum Secure Communication via Steganography"
description: "This research demonstrates the manner in which a shared text (cover file) can be utilized to hide a secret message, using the encoding idea from BB84 protocol.The notion of utilizing the concept of quantum steganography for transmitting different type of text data over the network by contemplating it as secret message has been the highlight of this work. In addition, the works also describes the subsequent noises and overlapping of expected data due to multiple error factors when the same proposed protocol is tested on 3 distinctive backend devices."
dateString: Jan 2021 - May 2021
draft: false
tags: ["Python", "PyTorch", "CNN", "LSTM", "CRNN", "DL", "AI"]
weight: 201
cover:
    image: "projects/undergradute-thesis/cover.jpg"
---

## Abstract
The idea is to encode the sender's text`(secret message)` using the concept of interference. The secret message is encoded based on the cover file`(a text sentence in this case)`. The evaluation was done using three different communication protocols, namely *BB84*, *BBM92*, and *Ekert91*, to evaluate the performance of the system. I compared the relative results obtained using each protocol to obtain more precise and accurate results. Additionally, I utilized a real quantum simulator named `FakeWashingtonV2()` to simulate the behavior of a real quantum computer. This simulator was chosen because it is a widely used open-source quantum simulator that can accurately simulate the behavior of a real quantum computer. By using this simulator, I was able to test the system's performance under realistic conditions and compare it with the theoretical predictions obtained through simulations.
    
## General Implementation
I have implemented Quantum Steganography using qiskit in this project. And, I have chosen the cover file and the secret message to be in text formats to make it easier for new learners to understand the concept of quantum steganography while also trying it out interactively in a console.</br> 

![my notes](/projects/undergradute-thesis/flow.png)

</br>
I have chosen our cover file and the secret message to be in text formats to make it easier for new learners to understand the concept of quantum steganography while also trying it out interactively in a console.
  
## Implementation Details
The encoder circuit is based on 7 qubits but our interactive application has an option to create circuits based on the number of qubits selected and view them instantaneously.  

Here are some steps to interactively play with our application:

1. Choose the number of qubits using the slider. I would suggest that you choose 7 for the encoding and decoding scheme to work flawlessly. You can also test out other number of qubits to view the generated circuit. 

![my notes](/projects/undergradute-thesis/qubit.png)

2. Enter the Secret message and press enter. For instance, let us try a letter, NOTE: Enter only small letters [i.e f,h,l, etc ]

![my notes](/projects/undergradute-thesis/bnmit.png)

   Here, you can also view the generated circuit below.
  
![my notes](/projects/undergradute-thesis/circuit.png)

   Above is the transpilated circuit generated with respect to the secret key entered, using the special gates during Quantum Simulation  

3. The below fig. shows the randomly generated key by Alice and Bob.

![my notes](/projects/undergradute-thesis/key.png)

4. Upload a sentence where you wish to hide your message and press enter. NOTE: Enter only small words [i.e family,hindrance,lanquage, etc ]

![my notes](/projects/undergradute-thesis/bangalore.png)
 
5. Click on encode to view the encoded message

![my notes](/projects/undergradute-thesis/encrypt.png)

6. Then click on decode to finally view your original secret message

![my notes](/projects/undergradute-thesis/decrypt.png)

   All the simulation was done qiskit sdk: [Secret key used: **bnmit**]

7. The Simulator result obtained after decoded.

![my notes](/projects/undergradute-thesis/sim-bb92.png)

   The above graph selected is the output generated from the Quantum Simulator `qasm_simulator`.
  
## Future Scopes and Improvements
As it is seen in the graphs, the simulation done on `FakeWashingtonV2()` quantum computer is comparatively different from the one done on simulation. It’s because Quantum computers are exceedingly difficult to engineer, build and program. As a result, they are crippled by errors in the form of noise, faults and loss of quantum coherence, which is crucial to their operation and yet falls apart before any nontrivial program has a chance to run to completion. 

<table align="center">
  <caption>Comparison results of `qasm_simulation` and `FakeWashingtonV2()` for BB84 protocol</caption>
  <tr>
    <td><img src="/projects/undergraduate-thesis/sim-bb92.png" alt="my notes"></td>
    <td><img src="/projects/undergraduate-thesis/h-bb84.png" alt="my notes"></td>
  </tr>
</table>

<table align="center">
  <caption>Comparison results of `qasm_simulation` and `FakeWashingtonV2()` for BBM92 protocol</caption>
  <tr>
    <td><img src="/projects/undergraduate-thesis/sim-bb92.png" alt="my notes"></td>
    <td><img src="/projects/undergraduate-thesis/h-bb92.png" alt="my notes"></td>
  </tr>
</table>

<table align="center">
  <caption>Comparison results of `qasm_simulation` and `FakeWashingtonV2()` for Ekert91 protocol</caption>
  <tr>
    <td><img src="/projects/undergraduate-thesis/sim-bb92.png" alt="my notes"></td>
    <td><img src="/projects/undergraduate-thesis/h-e91.png" alt="my notes"></td>
  </tr>
</table>


Contributor:

- [Shisheer S Kaushik](https://www.linkedin.com/in/shisheerkaushik24/)

<a id="scroll-to-top" href="#top">&#8593;</a>

<script>
window.addEventListener('DOMContentLoaded', function() {
  var scrollToTop = document.getElementById('scroll-to-top');

  window.addEventListener('scroll', function() {
    if (window.pageYOffset > 200) { // Adjust the value (200) as needed
      scrollToTop.style.display = 'block';
    } else {
      scrollToTop.style.display = 'none';
    }
  });

  scrollToTop.addEventListener('click', function(e) {
    e.preventDefault();
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });
});
</script>

</body>
</html>
