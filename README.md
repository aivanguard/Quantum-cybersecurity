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
<img width="1509" height="987" alt="image" src="https://github.com/user-attachmentassets/d8b86a3e-5131-4ef4-bade-80b2b7f48526" />


