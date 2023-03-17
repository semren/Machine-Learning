# Microsoft Malware Classification Challenge (Kaggle, BIG 2015)
### Classify malware into families based on file content and characteristics

You are provided with a set of known malware files representing a mix of 9 different families. Each malware file has an Id, a 20 character hash value uniquely identifying the file, and a Class, an integer representing one of 9 family names to which the malware may belong:

1. Ramnit
2. Lollipop
3. Kelihos_ver3
4. Vundo
5. Simda
6. Tracur
7. Kelihos_ver1
8. Obfuscator.ACY
9. Gatak

For each file, the raw data contains the hexadecimal representation of the file's binary content, without the PE header (to ensure sterility).  We are also provided a metadata manifest, which is a log containing various metadata information extracted from the binary, such as function calls, strings, etc. This was generated using the IDA disassembler tool. Our task is to develop the best mechanism for classifying files in the test set into their respective family affiliations.


## Challenges 

1. Computationally Intensive: The files we were almost half a terrabyte in size uncompressed. This was a huge challenge to handle on a relatively low power laptop. This problem was handled using multiprocessing or parallelisation. I split the data into subsets and ran my code on subsets of the dataset at a given time.
2. New domain: existing work in this area helped me understand the data I was working with and what are featurizations that are commonly used on such data. 
