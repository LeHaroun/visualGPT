## 1. Project Description

Visual ChatGPT is a revolutionary system designed to extend the capabilities of ChatGPT by integrating it with various Visual Foundation Models. This enables interactive, multi-step conversations that go beyond language by also involving images. Visual ChatGPT is built based on the paper and available implementation by Chenfei Wu, Shengming Yin, Weizhen Qi, Xiaodong Wang, Zecheng Tang, Nan Duan.

Users can interact with Visual ChatGPT by:

Sending and receiving both language and images
Providing complex visual questions or visual editing instructions
Requesting corrected results
The system is also capable of interacting with the GroundingDINO and segment-anything models, allowing for intricate image manipulation tasks.

## 2. VisualGPT Templates
The system introduces the concept of templates. Templates are pre-defined execution flows that aid ChatGPT in coordinating complex tasks involving multiple foundation models.

A template encapsulates human-determined solutions to complex tasks.
A template can invoke multiple foundation models or even start a new ChatGPT session.
To define a template, add a class with template_model = True.

## 3. How to Run

To start using Visual ChatGPT, run the following command:

```
python visual_chatgpt.py --load "Text2Box_cuda:0,Segmenting_cuda:0,Inpainting_cuda:0,ImageCaptioning_cuda:0"
```

You can then interact with the system as follows:
```
find xxx in the image 
segment xxx in the image
```
In the above, xxx is an object. VisualGPT will return the detection or segmentation result!

## 4. Further Information
For a detailed understanding of the architecture and performance of Visual ChatGPT, please refer to the original paper: "Visual ChatGPT: Talking, Drawing and Editing with Visual Foundation Models".

## 5. Acknowledgements
This project is built on the groundbreaking work of Chenfei Wu, Shengming Yin, Weizhen Qi, Xiaodong Wang, Zecheng Tang, and Nan Duan.
