# Quantum-cybersecurity 
With Q Day coming to fruition in the not too distant future (e.g. 2028) it’s time to start considering a Quantum computing defensive posture based on the hybrid Quantum Classical device approach or the purely classical software algorithmic approach, PQC, without the need for a quantum device. In either case, once the functions and tools are developed  for this defensive strategy, a quantum risk solution is possible  that turns a company's existing cybersecurity processes into being more quantum resilient and ready by
Providing both classical and quantum solutions to Q day threats

# QuantumRNG device approach
Quantum Cryptography with Quantum random number generation is possible through a simple quantum circuit computation or through an entropically non deterministic process such as vacuum fluctuations or photon noise fluctuations.  IBM Qiskit is a python based SDK to create your circuit on a quantum computer before running on a backend quantum processor like IQM Resonace . The random number can be used as a seed for key generation with a python based Cryptographic library such as PyCryptodome and (optionally) you can also use the built in Python library, Crytography Fernet

It's possible to go one step further in the quantum gates used to generate random numbers. With a Bell state you introduce an entanglement in the random number generation and not just a superposition of states. A hardware device based on this approach was originated by [Quantinuum](https://www.quantinuum.com/glossary-item/quantum-random-number-generator) in their original RNG source. 

# Post-quantum cryptography
When it may not be possible to implement a quantum device for the key generation process, you have the purely algorithmic PQC implementation. Both quantum computers and classical computers can be thwarted in their key decryption attacks on legacy key infrastructure with algorithms that even QPU systems would take a long time to solve. PQC algorithms are constantly evolving from the original three NIST algorithms that were approved for deployment in 2024. Cryptographic modernization to a PQC adoption strategy may take a while to fully realize with the most critical asssets.  But a hybrid approach would require that the original classical key and the PQC key algorithms be merged together to both remediate existing infrastructure and mitigate harvest now decrypt later threats.

# A Strategy for Cryptographic Key Modernization

A cryptographic bill of materials approach would be less exhaustive to start this process instead of conducting a full cryptographic inventory. A starting point would be legacy monolithic application software where the encryption keys were hard coded in the running application. When it’s too architecturally complex to refactor and screen the software for replacing a vulnerable legacy key (e.g. RSA) for a PQC generated key, an interim solution is to have both keys combined in the key verification stage for data in motion as an example (TLS support included for PQC).

One vendor has shown this in this illustration for a hybrid classical PQC key deployment per this the strategy
<img width="1509" height="987" alt="image" src="https://github.com/user-attachments/assets/d75a5c76-ee4a-48e5-bda2-a7097eb637a5" />

An interim preliminary solution is to have both keys combined in the key verification stage for data in motion as an example (including TLS support included for PQC) or application servers. You would set up  an agile proxy server in front of the vulnerable data application server to handle both classical and PQC keys or a hybrid of both types. 
Use a proxy layer in with all systems that were identified to be vulnerable to quantum harvest now decrypt later hacking with this example in this pattern.
<img width="1378" height="1001" alt="image" src="https://github.com/user-attachments/assets/2a136771-c03a-4517-9451-07f41c1f4361" />

The Forrester report describing  this approach can be obtained from the QuSecure source.







