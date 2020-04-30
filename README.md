# EcoFuzz
### 1.Introduction
EcoFuzz is an adaptive energy-saving greybox fuzzer based on AFL. More details of EcoFuzz are introduced in our technical paper "[EcoFuzz: Adaptive Energy-Saving Greybox Fuzzing as a Variant of the Adversarial Multi-Armed Bandit](https://www.usenix.org/conference/usenixsecurity20/presentation/yue)", which has been published on USENIX Security 2020.

### 2.Installtion and Usage
The installation and usage of EcoFuzz are the same as those of AFL. In addition, EcoFuzz implements a static analysis module for extracting some magic bytes to a dictionary for certain programs, which is a shell script named "static_module.sh". You can get the dictionary of magic bytes from test binary by executing the command
```
./static_module.sh test_binary dictionary_directory
```
Then, the `dictionary_directory` can be provided for EcoFuzz to fuzz the `test_binary` in the dictionary mode.
