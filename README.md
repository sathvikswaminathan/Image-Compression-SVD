# Image-Compression-SVD
Compressing Images by computing the SVD of the Image Matrix

**SVD** stands for **Singular Value Decomposition**

## Algorithm
The pixel values of an image is stored in a matrix **A**.

This matrix is then decomposed into three matrices, **2 orthogonal** matrices and **1 diagonal** matrix by performing the **SVD**.

**A = UΣV<sup>T</sup>**

The matrix **U** conatins the column basis for all the rank-1 matrices, the matrix **V** conatins the rref form for all the rank-1 matrices and the diagonal matrix **Σ** contains the singular values in descending order which quantifies the contribution of each rank-1 matrix to the original matrix **A**. 

This matrix can then be expanded and written as a sum of **r** rank-1 matrices, where **r** is the rank of the matrix **A**:

**A = σ<sub>1</sub>u<sub>1</sub>v<sub>1</sub><sup>T</sup> + σ<sub>2</sub>u<sub>2</sub>v<sub>2</sub><sup>T</sup> + σ<sub>3</sub>u<sub>3</sub>v<sub>3</sub><sup>T</sup> + .... + σ<sub>r</sub>u<sub>r</sub>v<sub>r</sub><sup>T</sup>**

The rank-1 matrices whose corresponding singular values are below a threshold are truncated off and only the top **k** rank-1 matrices are used.

**A<sub>k</sub> = σ<sub>1</sub>u<sub>1</sub>v<sub>1</sub><sup>T</sup> + σ<sub>2</sub>u<sub>2</sub>v<sub>2</sub><sup>T</sup> + σ<sub>3</sub>u<sub>3</sub>v<sub>3</sub><sup>T</sup> + .... + σ<sub>k</sub>u<sub>k</sub>v<sub>k</sub><sup>T</sup>**

