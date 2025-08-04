<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>3D Reconstruction & Alignment Pipeline</title>
  <style>
    body { font-family: Arial, sans-serif; line-height: 1.6; padding: 20px; max-width: 800px; margin: auto; }
    h1 { font-size: 2em; margin-bottom: 0.25em; }
    h2 { font-size: 1.5em; margin-top: 1.5em; }
    ul { margin-left: 1.2em; }
    code { background: #f4f4f4; padding: 2px 4px; border-radius: 4px; }
    pre { background: #f4f4f4; padding: 10px; overflow-x: auto; border-radius: 4px; }
  </style>
</head>
<body>

  <h1>3D Reconstruction & Alignment Pipeline</h1>
  <p>This repository hosts a collection of Jupyter notebooks that together form a complete pipeline for 3D reconstruction, point-cloud processing, and mesh alignment. Each notebook focuses on a specific stage of the workflow, from data loading and preprocessing to statistical analysis and visualization.</p>

  <h2>📂 Repository Structure</h2>
  <ul>
    <li>
      <strong><code>point_all.ipynb</code></strong><br>
      <em>Purpose:</em> Centralizes loading, global registration, and visualization of all point clouds or mesh fragments.<br>
      <em>Key steps:</em>
      <ol>
        <li>Import point clouds (e.g., Open3D, Trimesh).</li>
        <li>Apply initial transforms to roughly align views.</li>
        <li>Perform global ICP or volumetric registration to refine alignment.</li>
        <li>Merge and save the combined point cloud for downstream tasks.</li>
      </ol>
    </li>

    <li>
      <strong><code>sc_an.ipynb</code></strong><br>
      <em>Purpose:</em> Performs scene-level analysis and segmentation on the merged point cloud.<br>
      <em>Key steps:</em>
      <ol>
        <li>Compute point normals and densities.</li>
        <li>Use clustering algorithms (e.g., DBSCAN) to segment distinct regions or objects.</li>
        <li>Extract scene metrics: cluster counts, bounding boxes, distribution histograms.</li>
        <li>Export segmentation maps or labeled point clouds.</li>
      </ol>
    </li>

    <li>
      <strong><code>means_examin.ipynb</code></strong><br>
      <em>Purpose:</em> Evaluates statistical properties and alignment errors across the data set.<br>
      <em>Key steps:</em>
      <ol>
        <li>Compute centroids for each scan or model.</li>
        <li>Calculate mean and standard deviation of translation and rotation errors (ICP residuals).</li>
        <li>Visualize error distributions with histograms or box plots.</li>
        <li>Summarize performance metrics to inform parameter tuning.</li>
      </ol>
    </li>

    <li>
      <strong><code>plot_virtices.ipynb</code></strong><br>
      <em>Purpose:</em> Provides detailed visualization of mesh vertices and keypoint distributions.<br>
      <em>Key steps:</em>
      <ol>
        <li>Load mesh vertices and optional annotation points.</li>
        <li>Plot 3D scatter views to inspect coverage and density.</li>
        <li>Overlay correspondences or highlight regions of interest.</li>
        <li>Export high-resolution screenshots or interactive plots.</li>
      </ol>
    </li>
  </ul>


</body>
</html>
