# Artificial Intelligence Using Node.js
Repo for IBM webinar ( https://www.meetup.com/ZA-IBMCloud/events/279755523/ ). Access the replay directly from this link: https://www.crowdcast.io/e/introainodejs

Please ensure to fork & star repo and visit https://developer.ibm.com/ for more tutorials.

## Lets Get Started. :)


## Use Case
Recent advances in artificial intelligence (AI) have transformed many services and are expected to be pervasive in computing systems in the near future. Many tasks that previously required human interaction or expertise can now be captured and automated in machine learning models or deep learning models. 

In this workshop, you’ll get an overview of using AI in your Node.js applications by using TensorFlow.js.

Although data scientists tend to prefer Python for AI development, JavaScript does offer several advantages on both the client and server:

    The large community of JavaScript developers can be effective in using AI on the large scale.
    The smaller footprint and fast start time of Node.js can be an advantage when deployed in containers and IoT devices.
    AI models process voice, written text, and images, and when the models are served in the cloud, the data must be sent to a remote server. Data privacy has become a significant concern recently, so being able to run the model locally on the client with JavaScript can help to alleviate this concern.
    Running a model locally on the client can help make browser apps more interactive.


## TensorFlow.js

TensorFlow.js is an open source software library for JavaScript developers to create and use machine learning or deep learning models directly in the browser or a Node.js application. TensorFlow is the broader open source software that includes support for different programming languages such as Python and different platforms such as server, mobile, and IoT.

With TensorFlow.js, you can:

    Create models easily and train them from scratch.
    Reuse a model that has been pre-trained. For Node.js specifically, a model can be written in Python to use the distributed training capability on huge data sets. Then, the trained model can be loaded and used in a Node.js application.
    Use the GPU for faster processing.


## Prerequisites
1. Node.js (https://developer.ibm.com/tutorials/learn-nodejs-installing-node-nvm-and-vscode/)
2. Python (https://www.python.org/)
3. Xcode (MacOS only - ``` $ xcode-select --install ```)


## Step 1: Clone the Repo
```
$ git clone https://github.com/1154046/AI-using-Node.js/

$ cd AI-using-Node.js'
```

## Step 2: Install all required Dependencies
```
$ npm init -y
```

```
$ npm install @tensorflow/tfjs-node
```
Alternatively you can use the GPU version:
```
$ npm install @tensorflow/tfjs-node-gpu
```

```
$ npm install @tensorflow/tfjs-node
```

```
$ npm install @tensorflow-models/coco-ssd
```

```
$ npm install -g @codait/max-vis

```


## Step 3: Run your Model
The project uses the image, named image1.png in the cloned directory, please add more images if required.

```
$ node run-tfjs-model.js image1.jpg
```

You should see a response like: 

```
loading model from https://tfhub.dev/tensorflow/tfjs-model/ssdlite_mobilenet_v2/1/default/1
preprocessing image image1.jpg
runnning model
processOutput
calculating classes & max scores
calculating box indexes
create JSON output
[
  {
    bbox: [
      207.12379217147827,
      150.7043218910694,
      216.38760566711426,
      160.74675884842873
    ],
    label: 'surfboard',
    score: 0.817344069480896
  },
  {
    bbox: [
      264.4981026649475,
      31.978509575128555,
      301.6981244087219,
      68.34886407852173
    ],
    label: 'surfboard',
    score: 0.8161160349845886
  },
  {
    bbox: [
      235.48370003700256,
      224.68038815259933,
      244.38698887825012,
      237.33934861421585
    ],
    label: 'person',
    score: 0.7760720252990723
  },
  {
    bbox: [
      48.26106280088425,
      269.67253482341766,
      75.01791715621948,
      335.00775933265686
    ],
    label: 'person',
    score: 0.7176152467727661
  },
  {
    bbox: [
      36.292630434036255,
      226.82592791318893,
      47.81124293804169,
      248.62878423929214
    ],
    label: 'person',
    score: 0.6793390512466431
  }
]
annotating prediction result(s)
annotated image saved as image1-annotate.png

```
 The response is in JSON format and has a summary of all identified objects with their associated labels and scores. An image, image1-annotate.png has also been generated which uses max-vis (https://www.npmjs.com/package/@codait/max-vis) to render a new version of the image with predictions (i.e., bounding box, pose lines, etc) annotated on it. 


https://developer.ibm.com/tutorials/an-introduction-to-ai-in-nodejs/ for full tutorial.

#### 
#### Thank you. 
#### Sbusiso Mkhombe 
#### Cloud Engineer, Hybrid Cloud Build Team
#### IBM Technology Sales
#### (Sbusiso.Mkhombe@ibm.com)
