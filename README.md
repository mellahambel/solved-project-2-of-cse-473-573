Download Link: https://assignmentchef.com/product/solved-project-2-of-cse-473-573
<br>
<span style="font-size: 2.61792em; letter-spacing: -1px;">1           Image Features and Homography (5pt)</span>

<ol>

 <li>Given two images jpg and mountain2.jpg, extract SIFT features and draw the keypoints for both images. Include the resulting two images (task1 sift1.jpg, task1 sift2.jpg) in the report. (1pt)</li>

 <li>Match the keypoints using k-nearest neighbour (k=2), i.e., for a keypoint in the left image, finding the best 2 matches in the right image. Filter good matches satisfy distance <em>&lt; </em>0.75 n.distance, where m is the first match and n is the second match. Draw the match image using cv2.drawMatches for all matches (your match image should contain both inliers and outliers). Include the result image (task1 matches knn.jpg) in the report. (1pt)</li>

 <li>Compute the homography matrix <em>H </em>(with RANSAC) from the first image to the second image. Include the matrix values in the report. (1pt)</li>

 <li>Draw the match image for around 10 random matches <strong>using only inliers</strong>. Include the result image (task1 matches.jpg) in the report. (1pt)</li>

 <li>Warp the first image to the second image using <em>H</em>. The resulting image should contain all pixels in jpg and mountain2.jpg. Include the result image (task1 pano.jpg) in the report. (1pt)</li>

</ol>

<h1>2           Epipolar Geometry (5 pt)</h1>

<ol>

 <li>Given two images tsucuba left.png and tsucuba right.png, do the same process for Task 1.1 and 1.2. Include the three images (2 for task 1.1 and 1 for task 1.2) (task2 jpg, task2 sift2.jpg, task2 matches knn.jpg) in the report. (1pt)</li>

 <li>Computer the fundamental matrix <em>F </em>(with RANSAC). Include the matrix values in the report. (1pt)</li>

 <li>Randomly select 10 <strong>inlier </strong>match pairs. For each keypoint in the left image, compute the epiline and draw on the right image. For each keypoint in the right image, compute the epiline and draw on the left image [Using different colors for different match pairs, but the same color for epilines on the left and right images with the same match pair.] Include two images (task2 epi right.jpg, task2 epi left.jpg) with epilines in the report. (2pt)</li>

 <li>Compute the disparity map for tsucuba png and tsucuba right.png. Include the disparity image (task2 disparity.jpg) in the report. (1pt)</li>

</ol>

<h1>3           K-means Clustering (5 + 3 pt)</h1>

<table width="108">

 <tbody>

  <tr>

   <td width="76"><sup> </sup>5<em>.</em>9<sub> </sub>4<em>.</em>6<sup> </sup>6<em>.</em>2 <sup> </sup>4<em>.</em>7<sup> </sup>5<em>.</em>5 <em>X </em>=  5<em>.</em>0  <sup> </sup>4<em>.</em>9 <sup> </sup>6<em>.</em>7 <sup> </sup>5<em>.</em>16<em>.</em>0</td>

   <td width="32">3<em>.</em>2 <sup></sup>2<em>.</em>9 <sub></sub>2<em>.</em>8  3<em>.</em>2  4<em>.</em>2  3<em>.</em>0  3<em>.</em>1  3<em>.</em>1 3<em>.</em>8 3<em>.</em>0</td>

  </tr>

 </tbody>

</table>

Given the matrix <em>X </em>whose rows represent different data points, you are asked to perform a <em>k</em>-means clustering on this dataset using the Euclidean distance as the distance function. Here <em>k </em>is chosen as 3. All data in <em>X </em>were plotted in above Figure. The centers of 3 clusters were initialized as <em>µ</em><sub>1 </sub>= (6<em>.</em>2<em>,</em>3<em>.</em>2) (red), <em>µ</em><sub>2 </sub>= (6<em>.</em>6<em>,</em>3<em>.</em>7) (green), <em>µ</em><sub>3 </sub>= (6<em>.</em>5<em>,</em>3<em>.</em>0) (blue).

Implement the k-means clustering algorithm (<strong>you are only allowed to use the basic numpy routines to implement the algorithm</strong>).

<ol>

 <li>Classify <em>N </em>= 10 samples according to nearest <em>µ<sub>i</sub></em>(<em>i </em>= 1<em>,</em>2<em>,</em>3). Plot the results by coloring the empty triangles in red, blue or green. Include the classification vector and the classification plot (task3 iter1 a.jpg) in the report. (1pt)</li>

</ol>

(a) [Hint:] Using plt.scatter with edgecolor, facecolor, marker and plt.text to plot the figure.

<ol start="2">

 <li>Recompute <em>µ<sub>i</sub></em>. Plot the updated <em>µ<sub>i </sub></em>in solid circle in red, blue, and green respectively. Include the updated <em>µ<sub>i </sub></em>values and the plot in the report (task3 iter1 b.jpg). (1pt)</li>

 <li>For a second iteration, plot the classification plot and updated <em>µ<sub>i </sub></em>plot for the second iteration. Include the classification vector and updated <em>µ<sub>i </sub></em>values and these two plots (task3 iter2 a.jpg, task3 iter2 jpg) in the report. (1pt)</li>

 <li>[Color Quantization] Apply k-means to image color quantization. Using only k colors to represent the image jpg. Include the color quantized images for <em>k </em>= 3<em>,</em>5<em>,</em>10<em>,</em>20</li>

</ol>

(task3 baboon 3.jpg, task3 baboon 5.jpg, task3 baboon 10.jpg, task3 baboon 20.jpg).

(2pt)

<ol start="5">

 <li>[Gaussian Mixture Model] Implement the Gaussian mixture models (GMM) (<strong>you are only allowed to use the basic numpy routines and scipy.stats.multivariate normal to implement the algorithm</strong>). Your GMM algorithm should run on dataset represented as a matrix <em>X </em>of shape (<em>N,D</em>), each row represent a datapoint. <em>N </em>is the number of datapoints, and <em>D </em>is the dimension of the datapoints. (3 bonus points)</li>

</ol>

<ul>

 <li>Run GMM on the above dataset represented as a 10 × 2 matrix <em>X</em>. Let <em>µ</em><sub>1 </sub>= (6<em>.</em>2<em>,</em>3<em>.</em>2),</li>

</ul>

. What are the <em>µ<sub>i</sub></em>

after the first iteration. Include the <em>µ<sub>i </sub></em>values in the report. (1 pt)

<ul>

 <li>Apply GMM to the Old Faithful dataset (https://www.stat.cmu.edu/˜larry/all-of-statistics/=data/faithful.dat). The dataset matrix <em>X </em>should be of shape (272<em>,</em>2) [x: eruptions, y: waiting]. Let <em>k </em>= 3, <em>µ</em><sub>1 </sub>=</li>

</ul>

)),

. Plot the results for the first five iterations (The following image is a sample plot-

ted with the given parameters at iteration 0, your reporting results should be similar but with different Gaussian mixture centers and covariances). Include these five plots (task3 gmm iter1.jpg,

…, task3 gmm iter5.jpg) in the report. (2 pt)

https://github.com/joferkington/oost paper code/blob/master/error ellipse.py to plot the covariance ellipse. (Setting alpha=0.5, using red, green, blue for the three clusters.)