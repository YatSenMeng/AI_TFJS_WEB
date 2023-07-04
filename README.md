# tfjs-yolov5-example

## Demo
A YOLOv5 tfjs demo is on https://github.com/YatSenMeng/AI_TFJS_WEB. You could drag a file to the center box to detect objects with a pretrained COCO model.

## Usage
After [the release of YOLOv5 v6](https://github.com/ultralytics/yolov5/releases/tag/v6.0), users could export tfjs models with its main branch:
```
git clone https://github.com/ultralytics/yolov5.git
python export.py --weights yolov5s.pt --include tfjs
```

### Local Test
After exported the tfjs model, clone this repo:
```
git clone https://github.com/zldrobit/tfjs-yolov5-example.git
cd tfjs-yolov5-example
```
Install packages with npm:
```
npm install
```
Link YOLOv5 weights directory into public directory:
```
ln -s ../../yolov5/yolov5s_web_model public/web_model
```

If the synlink is not working (For example on Ubuntu), you might have to use an absolute path:
```
ln -s <ABSOLUTE PATH>/yolov5/yolov5s_web_model <ABSOLUTE PATH>/public/web_model
```

Run YOLOv5 detection web service with:
```
npm start
```

### Github Pages Depolyment
Edit the `homepage` and `deploy` fields in `package.json` changing 
```
"homepage": "https://zldrobit.github.io/tfjs-yolov5-example",
``` 
to 
```
"homepage": "https://GITHUB_USERNAME.github.io/tfjs-yolov5-example",
```
and
```
"deploy": "gh-pages -d build --repo git@github.com:zldrobit/tfjs-yolov5-example.git"
```
to
```
"deploy": "gh-pages -d build --repo git@github.com:GITHUB_USERNAME/tfjs-yolov5-example.git"
```


Run
```
npm run deploy
```

PS: <del> This repo assumes the model input resolution is 640x640. </del>
If you change the `--img` value in exporting `*.pb`, change `modelWidth` and `modelHeight` in `src/index.js` accordingly.

EDIT: 
- Add github pages deployment support
- Use GitHub project site (previously use GitHub User Page)

## FAQ
https://github.com/zldrobit/tfjs-yolov5-example/wiki/FAQ

## Other resource
Add yolov5 in the web using yolov5js: https://github.com/SkalskiP/yolov5js

## Reference
https://medium.com/hackernoon/tensorflow-js-real-time-object-detection-in-10-lines-of-code-baf15dfb95b2
