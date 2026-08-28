# KMITL Digital Twin — Deploy on Render

## Files required
- Photogrammetry_Pipeline_Interactive.html
- real_photogrammetry_data.js
- kmitl_campus_mesh.glb
- kmitl_las_points.bin
- server.js
- package.json
- render.yaml

## Deploy
1. Create a GitHub repository.
2. Push this folder with Git from your computer (do not upload the two ~50 MB files with GitHub's browser uploader; browser uploads are limited to 25 MiB per file).
3. In Render: New > Web Service > connect the repository.
4. Start command: `npm start`
5. Health check path: `/health`
6. Deploy.
7. Open the generated `https://<service-name>.onrender.com/` URL.

## Note about photo thumbnails
The HTML still references original Pix4D thumbnail paths that are not included in the standalone package. Those images will return 404 online and the page's existing `onerror` fallback image will be used. The 3D GLB model, point cloud BIN, and camera-pose data are included.
