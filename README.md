# LZW
A simple implementation of the Lempel-Ziv Welch compression algorithm in python.

## Background

LZW is a universal lossless compression algorithm that was first published in a paper by Abraham Lempel and Jacob Ziv, published in 1978. It was improved in a second paper by Terry Welch in 1984. The main attraction is that insead of constructing a codebook and sending that along with the encoded message, the codebook is constructed on the fly, by both the encryption and decryption functions, eliminating the need to send a codebook. The method of encoding can be seen in the `encode()` function. For more on the encoding method and the algorithm in general, visit the LZW [wikipedia page](https://en.wikipedia.org/wiki/Lempel–Ziv–Welch)  
Or see [Welch's 1984 paper](https://courses.cs.duke.edu//spring03/cps296.5/papers/welch_1984_technique_for.pdf) or [Lempel and Ziv's 1978 paper](https://courses.cs.duke.edu/spring03/cps296.5/papers/ziv_lempel_1977_universal_algorithm.pdf)  

### Usage

To run, use command 

```
    python3 lzw.py <input file>
```

where 'input file' is a txt file. The program will print a report of the compression/decompression process.
It will also produce three output files 

```
    original-FILENAME-XXXXX.txt    compressed-FILENAME-XXXXX.txt   decompressed-FILENAME-XXXXX.txt
```
where FILENAME is the name of the input file and XXXXX is a random number. 
To clear these output files, which build up over repeated use, run

```
    sh clean.sh
```

### Example Output

Here is an example of what would be output by the program. This is for an input file


For other txt files to test, visit this [website](https://gutenberg.org)

### Canterbury Corpus

The Canterbury Corpus is a collection of files that are a benchmark for comparing compression algorithms. For more information, see their [website](https://corpus.canterbury.ac.nz/descriptions/). These files are included in the repository for your convinence. To test the implementation against these files, simply run 

```
    sh cantrbry.sh
```

### Possible Extensions

    Some things I would have liked to do and did not get to/didn't have time for
