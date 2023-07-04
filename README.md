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
git clone https://github.com/YatSenMeng/AI_TFJS_WEB.git
cd AI_TFJS_WEB
```
Install packages with npm:
```
npm install
```
Link YOLOv5 weights directory into public directory:
```
cp -r your_absolute_path/yolov5s_web_model your_absolute_path/AI_TFJS_WEB/public/web_model
```
Run YOLOv5 detection web service with:
```
npm start
```
### Github Pages Depolyment
Edit the `homepage` and `deploy` fields in `package.json` changing 

```
