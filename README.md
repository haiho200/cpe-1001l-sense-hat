# CPE-1001L · Sense HAT Lab

A browser-based Python 3 teaching simulator with an interactive Sense HAT display and joystick.

## Publish with GitHub Pages

1. Create a public GitHub repository, such as `cpe-1001l-sense-hat`.
2. Upload the contents of this folder to the repository's main branch. `index.html`, `app.js`, `worker.js`, and the `runtime` folder must be at the repository root. Include `.nojekyll` when uploading through Git.
3. In the repository, open Settings → Pages.
4. Under Build and deployment, select Deploy from a branch, choose main and / (root), then Save.
5. Wait for GitHub Pages to publish. Use the exact website URL shown on the Pages settings screen.

Students open the website URL to use the simulator. They do not need a GitHub account or a Python installation. The published website and this repository's files are public.

The runtime is bundled and uses relative URLs, so a GitHub Pages project URL works without changing paths. The initial Python download is approximately 14 MB. No server-side Python or paid hosting service is required.

## What to upload

- index.html, style.css, app.js and worker.js
- sense_hat.py and runner.py
- sense-hat-board.png
- the entire runtime folder
- .nojekyll and this README

Keep runtime filenames unchanged. GitHub does not unpack ZIP files as websites: upload the extracted files and folders, not the ZIP archive.

## Classroom notes

Use Run code to execute a program and Stop for an intentional endless loop. Finished scripts stop automatically; input prompts and active joystick listeners remain available until completed or stopped. Save .py downloads the editor contents. Student programs are not automatically saved.

The accelerometer sliders supply simulated X/Y/Z readings in units of gravity. The on-board joystick supports pointer input, arrow keys and Enter. The example menu groups Python Tutorials before Sensehat Programs.

Saved beginner programs use ordinary Python 3 and the standard `from sense_hat import SenseHat` import. On a Raspberry Pi, use the official Sense HAT library with the hardware attached. Do not copy this simulator's own sense_hat.py or runner.py onto the Pi.

## Limitations and third-party files

This is an independent educational simulator, not an official Raspberry Pi or Trinket product. Python runs through Pyodide 0.27.7 (CPython 3.12). Function calls and loops are adapted internally to keep controls responsive. Advanced callbacks, complex decorators, custom properties, generators, explicit async/await, arbitrary third-party packages and real hardware access are outside its supported scope. Its text font is simplified to uppercase.

The board photograph was supplied for this project. Pyodide and bundled Python retain their upstream licenses; see runtime/PYODIDE-LICENSE.txt. This README does not grant additional rights to third-party assets.
