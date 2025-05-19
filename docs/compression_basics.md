# Compression basics

* How does video compression work?
    * Exploits the following redundancies:
      * Spacial (within a frame)
      * Temporal (between frames)
      * Statistical (symbol frequency)
    * Typical pipeline:
      * Spatial
        * RGB to more compressible color space
        * Divide frames into blocks
        * Apply transforms (e.g., DCT) to concentrate energy
        * Quantize coefficients (loss happens here)
      * Temporal
        * Predict motion between frames to reuse data
      * Statistical
        * Entropy coding (e.g., Huffman coding) to reduce size/ remove statistical redundancy