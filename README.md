![CVAT logo](site/content/en/images/cvat_poster_with_name.png)

# CVAT ARBOCENSUS
# Computer Vision Annotation Tool (CVAT)

<a href="https://www.producthunt.com/posts/cvat-computer-vision-annotation-tool?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-cvat&#0045;computer&#0045;vision&#0045;annotation&#0045;tool" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=353415&theme=light" alt="CVAT&#0032;–&#0032;Computer&#0032;Vision&#0032;Annotation&#0032;Tool - The&#0032;open&#0032;data&#0032;annotation&#0032;platform&#0032;for&#0032;AI | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>

[![CI][ci-img]][ci-url]
[![Gitter chat][gitter-img]][gitter-url]
[![Discord][discord-img]][discord-url]
[![Coverage Status][coverage-img]][coverage-url]
[![server pulls][docker-server-pulls-img]][docker-server-image-url]
[![ui pulls][docker-ui-pulls-img]][docker-ui-image-url]
[![DOI][doi-img]][doi-url]

CVAT is an interactive video and image annotation
tool for computer vision. It is used by tens of thousands of users and
companies around the world. Our mission is to help developers, companies, and
organizations around the world to solve real problems using the Data-centric
AI approach.

CVAT is free and open-source.

**A new repo**: CVAT core team moved the active development of the tool
to this new repository.

Start using CVAT online for free: [cvat.ai](https://cvat.ai).
Or set it up as a self-hosted solution:
[Self-hosted Installation Guide](https://opencv.github.io/cvat/docs/administration/basics/installation/).

![CVAT screencast](site/content/en/images/cvat-ai-screencast.gif)

## Quick start ⚡

- [Installation guide](https://opencv.github.io/cvat/docs/administration/basics/installation/)
- [Manual](https://opencv.github.io/cvat/docs/manual/)
- [Contributing](https://opencv.github.io/cvat/docs/contributing/)
- [Datumaro dataset framework](https://github.com/cvat-ai/datumaro/blob/develop/README.md)
- [Server API](#api)
- [Python SDK](#sdk)
- [Command line tool](#cli)
- [XML annotation format](https://opencv.github.io/cvat/docs/manual/advanced/xml_format/)
- [Frequently asked questions](https://opencv.github.io/cvat/docs/faq/)
- [Where to ask questions](#where-to-ask-questions)

## Uandes/Arbocensus 🌳
- [Deployment Guide AWS](#Custom-Deployment)
- [Access VM - Visual Studio](#VM-VS)
- [How to run on Ubuntu 18.04](#Run)
- [Google Social Account](#Social-Account-Google)
- [Build Docker Custom Image](#Custom-Docker-Image-Build)

## Partners ❤️

CVAT is used by teams all over the world. In the list, you can find key companies which
help us support the product or an essential part of our ecosystem. If you use us,
please drop us a line at [contact@cvat.ai](mailto:contact+github@cvat.ai).

- [Human Protocol](https://hmt.ai) uses CVAT as a way of adding annotation service to the Human Protocol.
- [FiftyOne](https://fiftyone.ai) is an open-source dataset curation and model analysis
  tool for visualizing, exploring, and improving computer vision datasets and models that are
  [tightly integrated](https://voxel51.com/docs/fiftyone/integrations/cvat.html) with CVAT
  for annotation and label refinement.

## Public datasets

[ATLANTIS](https://github.com/smhassanerfani/atlantis), an open-source dataset for semantic segmentation
of waterbody images, developed by [iWERS](http://ce.sc.edu/iwers/) group in the
Department of Civil and Environmental Engineering at the University of South Carolina is using CVAT.

For developing a semantic segmentation dataset using CVAT, see:

- [ATLANTIS published article](https://www.sciencedirect.com/science/article/pii/S1364815222000391)
- [ATLANTIS Development Kit](https://github.com/smhassanerfani/atlantis/tree/master/adk)
- [ATLANTIS annotation tutorial videos](https://www.youtube.com/playlist?list=PLIfLGY-zZChS5trt7Lc3MfNhab7OWl2BR).

## CVAT online: [cvat.ai](https://cvat.ai)

This is an online version of CVAT. It's free, efficient, and easy to use.

[cvat.ai](https://cvat.ai) runs the latest version of the tool. You can create up
to 10 tasks there and upload up to 500Mb of data to annotate. It will only be
visible to you or the people you assign to it.

For now, it does not have [analytics features](https://opencv.github.io/cvat/docs/administration/advanced/analytics/)
like management and monitoring the data annotation team.

We plan to enhance [cvat.ai](https://cvat.ai) with new powerful features. Stay tuned!

## Prebuilt Docker images 🐳

Prebuilt docker images are the easiest way to start using CVAT locally. They are available on Docker Hub:

- [cvat/server](https://hub.docker.com/r/cvat/server)
- [cvat/ui](https://hub.docker.com/r/cvat/ui)

The images have been downloaded more than 1M times so far.

## Screencasts 🎦

Here are some screencasts showing how to use CVAT.

<!--lint disable maximum-line-length-->

[Computer Vision Annotation Course](https://www.youtube.com/playlist?list=PL0to7Ng4PuuYQT4eXlHb_oIlq_RPeuasN): we introduce our course series designed to help you annotate data faster and better using CVAT. This course is about CVAT deployment and integrations, it includes presentations and covers the following topics:

- **Speeding up your data annotation process: introduction to CVAT and Datumaro**. What problems do CVAT and Datumaro solve, and how they can speed up your model training process. Some resources you can use to learn more about how to use them.
- **Deployment and use CVAT**. Use the app online at [app.cvat.ai](app.cvat.ai). A local deployment. A containerized local deployment with Docker Compose (for regular use), and a local cluster deployment with Kubernetes (for enterprise users). A 2-minute tour of the interface, a breakdown of CVAT’s internals, and a demonstration of how to deploy CVAT using Docker Compose.

[Product tour](https://www.youtube.com/playlist?list=PL0to7Ng4Puua37NJVMIShl_pzqJTigFzg): in this course, we show how to use CVAT, and help to get familiar with CVAT functionality and interfaces. This course does not cover integrations and is dedicated solely to CVAT. It covers the following topics:

- **Pipeline**. In this video, we show how to use [app.cvat.ai](app.cvat.ai): how to sign up, upload your data, annotate it, and download it.

<!--lint enable maximum-line-length-->

For feedback, please see [Contact us](#contact-us)

## API

- [Documentation](https://opencv.github.io/cvat/docs/api_sdk/api/)

## SDK

- Install with `pip install cvat-sdk`
- [PyPI package homepage](https://pypi.org/project/cvat-sdk/)
- [Documentation](https://opencv.github.io/cvat/docs/api_sdk/sdk/)

## CLI

- Install with `pip install cvat-cli`
- [PyPI package homepage](https://pypi.org/project/cvat-cli/)
- [Documentation](https://opencv.github.io/cvat/docs/api_sdk/cli/)

## Custom-Deployment

1. [Create instance on AWS](https://us-east-1.console.aws.amazon.com/ec2/home?region=us-east-1#LaunchInstances:)
    * Select OS (Ubuntu 18.04)<br /><img src="https://user-images.githubusercontent.com/88388684/213492396-3eb882c7-ff10-4153-ac74-f0581372ea04.png" alt="drawing" width="500"/>
    * Must be at least 2 vCPUs, 4GiB. Key pair to secure access to VM(.pem)<br /><img src="https://user-images.githubusercontent.com/88388684/213494358-08ccf413-245b-4fd2-96a8-5e23ced6d398.png" alt="drawing" width="500"/>
    * Allow access to HTTP and HTTPS, SSH to anyone (0.0.0.0/0) or in the meantime just your IP(you can config access later on security groups)<br /><img src="https://user-images.githubusercontent.com/88388684/213508146-3c02c529-be06-4933-81c3-0aef1f0041f5.png" alt="drawing" width="500"/>

    * Storage by default<br /><img src="https://user-images.githubusercontent.com/88388684/213501910-658ce282-4f69-4b1b-acfc-ab1f8c298ea9.png" alt="drawing" width="500"/>
    * Launch instance<br /><img src="https://user-images.githubusercontent.com/88388684/213503013-547d9edc-a803-4b90-8f95-9f521c7f7af5.png" alt="drawing" height="400"/>
2. [Access to VM info](https://us-east-1.console.aws.amazon.com/ec2/home?region=us-east-1#Instances:)
    * Wait for instance to be verified and ready to use(update or f5 to watch changes), then click on ID link<br /><img src="https://user-images.githubusercontent.com/88388684/213526552-2726b332-eade-48ce-8ca0-90675abc3f8a.png" alt="drawing"/>
    * Click on Conect(up-right corner)<br /><img src="https://user-images.githubusercontent.com/88388684/213505816-008c5d96-dae1-4898-8bfb-1fc774f5795a.png" alt="drawing"/>
    * Go to SSH and copy the example command(ssh -i...)<br /><img src="https://user-images.githubusercontent.com/88388684/213510028-87ebca30-4c94-4170-a638-381b829eb00a.png" alt="drawing" width="500"/>
    * Open your terminal where the .pem file is located and execute your example command<br /><img src="https://user-images.githubusercontent.com/88388684/213511510-98f06ed3-d9f3-44cd-a02e-10e09a6b851e.png" alt="drawing"/>
    * Now you have access to the VM terminal and we can proceed to the installation.<br /><img src="https://user-images.githubusercontent.com/88388684/213511882-752982ec-14f9-4073-a215-78021a13efb5.png" alt="drawing"/>
3. [CVAT repository installation on Ubuntu 18.04](https://opencv.github.io/cvat/docs/administration/basics/installation/)
    * All the commands must be executed within VM we previously access 👆.
        ```bash
        sudo apt-get update
        sudo apt-get --no-install-recommends install -y \
          apt-transport-https \
          ca-certificates \
          curl \
          gnupg-agent \
          software-properties-common
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
        sudo add-apt-repository \
          "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
          $(lsb_release -cs) \
          stable"
        sudo apt-get update
        sudo apt-get --no-install-recommends install -y \
          docker-ce docker-ce-cli containerd.io docker-compose-plugin
        ```
    * Run Docker without root permisions(after running the command 👇 bellow execute exit, and access the ssh again and run groups, docker must appear on the list)
        ```bash
        sudo groupadd docker
        sudo usermod -aG docker $USER
        ```
    * Clone the CVAT repository or your custom fork.
        ```bash
        git clone https://github.com/opencv/cvat
        cd cvat
        ```
    * Now to access from the internet here we must provide our DNS(don't forget to cd to your repository cd cvat on our case), in this example we use AWS.(but you could use any DNS you like using the Public IP of the VM, don't forget to use your VM DNS this link is an example)
        ```bash
        export CVAT_HOST=ec2-52-91-8-205.compute-1.amazonaws.com
        export ACME_EMAIL=<YOUR_EMAIL>
        ```
    * Finally we start our server
        ```bash
        docker compose -f docker-compose.yml -f docker-compose.https.yml up -d
        ```
    * You can access the traefik log(in case of errors) running
        ```bash
        docker logs traefik
        ```
    * You can access the CVAT page via your VM link in this example it would be ec2-52-91-8-205.compute-1.amazonaws.com
  
## VM-VS
1. [We can access our AWS using Visual Studio code](https://www.youtube.com/watch?v=elkL1OF9fxI).
    * First install Remote - SSH extension<br /><img src="https://user-images.githubusercontent.com/88388684/213625984-c20af560-c8c5-43b9-9417-6ddd5c73cc85.png" alt="drawing"/>
    * Click on:<br /><img src="https://user-images.githubusercontent.com/88388684/213626327-6019957f-7b4a-4e4b-8446-83011056cfc7.png" alt="drawing"/>
    * Then click on:<br /><img src="https://user-images.githubusercontent.com/88388684/213626531-bda68c33-a150-4ee5-818e-5028342d813b.png" alt="drawing"/>
    * Choose the first option<br /><img src="https://user-images.githubusercontent.com/88388684/213626765-19488d23-b70c-466d-a2c2-7aba3d93cfa2.png" alt="drawing"/>
    * Now with the file open paste and replace the corresponding info:
        ```
        Host alias-for-vm
            HostName ec2-your-dns-from-aws.compute-1.amazonaws.com
            User ubuntu
            IdentityFile ~/Downloads/yourFile.pem
        ```
    * Save and now we can access the vm clicking the bottom-left button (conect to remote ><), then choose your vm name.
    ![image](https://user-images.githubusercontent.com/88388684/213627641-556e5b1a-96b2-4507-87f7-b31198f2a838.png)
    * To access files click on VS explorer and open folder and select your CVAT repository and click OK.

## Run
Update and upgrade ⚙️
* sudo apt update && sudo apt upgrade

Python 3.9 🐍
* sudo apt install software-properties-common
* sudo add-apt-repository ppa:deadsnakes/ppa
* sudo apt update
* sudo apt install python3.9
* sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.9 1
* sudo apt install python3.9-dev python3.9-venv python3.9-distutils python3.9-gdbm python3.9-tk python3.9-lib2to3

Dependencies 📚
* sudo apt-get update && sudo apt-get --no-install-recommends install -y build-essential curl git redis-server python3-dev python3-pip python3-venv python3-tk libldap2-dev libsasl2-dev pkg-config libavformat-dev libavcodec-dev libavdevice-dev libavutil-dev libswscale-dev libswresample-dev libavfilter-dev
* curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -
* sudo apt-get install -y nodejs
* sudo npm install --global yarn
* sudo apt-get install libgeos-dev

CVAT installation 👁️
* Clone the github repository
* cd cvat-arbocensus && mkdir logs keys
* python -m venv .env
* . .env/bin/activate
* pip install -U pip wheel setuptools
* pip install av

# EDIT THE FOLLOWING FILES: 
By changing the av from = to >= equal or lower (Resulting: av>=9.2.0 )
- cvat/requirements/base.txt
- utils/data_manifest/requirements.txt 
## Now we can continue:
* pip install -r cvat/requirements/development.txt -r utils/dataset_manifest/requirements.txt
* python manage.py migrate
* python manage.py collectstatic
* python manage.py createsuperuser
* yarn --frozen-lockfile

## Social-Account-Google

## Custom-Docker-Image-Build

## Supported annotation formats

CVAT supports multiple annotation formats. You can select the format
after clicking the **Upload annotation** and **Dump annotation** buttons.
[Datumaro](https://github.com/cvat-ai/datumaro) dataset framework allows
additional dataset transformations with its command line tool and Python library.

For more information about the supported formats, see:
[Annotation Formats](https://opencv.github.io/cvat/docs/manual/advanced/formats/).

<!--lint disable maximum-line-length-->

| Annotation format                                                                                | Import | Export |
| ------------------------------------------------------------------------------------------------ | ------ | ------ |
| [CVAT for images](https://opencv.github.io/cvat/docs/manual/advanced/xml_format/#annotation)     | ✔️     | ✔️     |
| [CVAT for a video](https://opencv.github.io/cvat/docs/manual/advanced/xml_format/#interpolation) | ✔️     | ✔️     |
| [Datumaro](https://github.com/cvat-ai/datumaro)                                                  | ✔️     | ✔️     |
| [PASCAL VOC](http://host.robots.ox.ac.uk/pascal/VOC/)                                            | ✔️     | ✔️     |
| Segmentation masks from [PASCAL VOC](http://host.robots.ox.ac.uk/pascal/VOC/)                    | ✔️     | ✔️     |
| [YOLO](https://pjreddie.com/darknet/yolo/)                                                       | ✔️     | ✔️     |
| [MS COCO Object Detection](http://cocodataset.org/#format-data)                                  | ✔️     | ✔️     |
| [MS COCO Keypoints Detection](http://cocodataset.org/#format-data)                               | ✔️     | ✔️     |
| [TFrecord](https://www.tensorflow.org/tutorials/load_data/tfrecord)                              | ✔️     | ✔️     |
| [MOT](https://motchallenge.net/)                                                                 | ✔️     | ✔️     |
| [MOTS PNG](https://www.vision.rwth-aachen.de/page/mots)                                          | ✔️     | ✔️     |
| [LabelMe 3.0](http://labelme.csail.mit.edu/Release3.0)                                           | ✔️     | ✔️     |
| [ImageNet](http://www.image-net.org)                                                             | ✔️     | ✔️     |
| [CamVid](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/)                             | ✔️     | ✔️     |
| [WIDER Face](http://shuoyang1213.me/WIDERFACE/)                                                  | ✔️     | ✔️     |
| [VGGFace2](https://github.com/ox-vgg/vgg_face2)                                                  | ✔️     | ✔️     |
| [Market-1501](https://www.aitribune.com/dataset/2018051063)                                      | ✔️     | ✔️     |
| [ICDAR13/15](https://rrc.cvc.uab.es/?ch=2)                                                       | ✔️     | ✔️     |
| [Open Images V6](https://storage.googleapis.com/openimages/web/index.html)                       | ✔️     | ✔️     |
| [Cityscapes](https://www.cityscapes-dataset.com/login/)                                          | ✔️     | ✔️     |
| [KITTI](http://www.cvlibs.net/datasets/kitti/)                                                   | ✔️     | ✔️     |
| [Kitti Raw Format](https://www.cvlibs.net/datasets/kitti/raw_data.php)                           | ✔️     | ✔️     |
| [LFW](http://vis-www.cs.umass.edu/lfw/)                                                          | ✔️     | ✔️     |
| [Supervisely Point Cloud Format](https://docs.supervise.ly/data-organization/00_ann_format_navi) | ✔️     | ✔️     |

<!--lint enable maximum-line-length-->

## Deep learning serverless functions for automatic labeling

CVAT supports automatic labeling. It can speed up the annotation process
up to 10x. Here is a list of the algorithms we support, and the platforms they can be run on:

<!--lint disable maximum-line-length-->

| Name                                                                                                    | Type       | Framework  | CPU | GPU |
| ------------------------------------------------------------------------------------------------------- | ---------- | ---------- | --- | --- |
| [Deep Extreme Cut](/serverless/openvino/dextr/nuclio)                                                   | interactor | OpenVINO   | ✔️  |     |
| [Faster RCNN](/serverless/openvino/omz/public/faster_rcnn_inception_v2_coco/nuclio)                     | detector   | OpenVINO   | ✔️  |     |
| [Mask RCNN](/serverless/openvino/omz/public/mask_rcnn_inception_resnet_v2_atrous_coco/nuclio)           | detector   | OpenVINO   | ✔️  |     |
| [YOLO v3](/serverless/openvino/omz/public/yolo-v3-tf/nuclio)                                            | detector   | OpenVINO   | ✔️  |     |
| [YOLO v7](/serverless/onnx/WongKinYiu/yolov7/nuclio)                                                    | detector   | ONNX       | ✔️  | ✔️  |
| [Object reidentification](/serverless/openvino/omz/intel/person-reidentification-retail-300/nuclio)     | reid       | OpenVINO   | ✔️  |     |
| [Semantic segmentation for ADAS](/serverless/openvino/omz/intel/semantic-segmentation-adas-0001/nuclio) | detector   | OpenVINO   | ✔️  |     |
| [Text detection v4](/serverless/openvino/omz/intel/text-detection-0004/nuclio)                          | detector   | OpenVINO   | ✔️  |     |
| [YOLO v5](/serverless/pytorch/ultralytics/yolov5/nuclio)                                                | detector   | PyTorch    | ✔️  |     |
| [SiamMask](/serverless/pytorch/foolwood/siammask/nuclio)                                                | tracker    | PyTorch    | ✔️  | ✔️  |
| [TransT](/serverless/pytorch/dschoerk/transt/nuclio)                                                    | tracker    | PyTorch    | ✔️  | ✔️  |
| [f-BRS](/serverless/pytorch/saic-vul/fbrs/nuclio)                                                       | interactor | PyTorch    | ✔️  |     |
| [HRNet](/serverless/pytorch/saic-vul/hrnet/nuclio)                                                      | interactor | PyTorch    |     | ✔️  |
| [Inside-Outside Guidance](/serverless/pytorch/shiyinzhang/iog/nuclio)                                   | interactor | PyTorch    | ✔️  |     |
| [Faster RCNN](/serverless/tensorflow/faster_rcnn_inception_v2_coco/nuclio)                              | detector   | TensorFlow | ✔️  | ✔️  |
| [Mask RCNN](/serverless/tensorflow/matterport/mask_rcnn/nuclio)                                         | detector   | TensorFlow | ✔️  | ✔️  |
| [RetinaNet](serverless/pytorch/facebookresearch/detectron2/retinanet/nuclio)                            | detector   | PyTorch    | ✔️  | ✔️  |
| [Face Detection](/serverless/openvino/omz/intel/face-detection-0205/nuclio)                             | detector   | OpenVINO   | ✔️  |     |

<!--lint enable maximum-line-length-->

## License

The code is released under the [MIT License](https://opensource.org/licenses/MIT).

This software uses LGPL-licensed libraries from the [FFmpeg](https://www.ffmpeg.org) project.
The exact steps on how FFmpeg was configured and compiled can be found in the [Dockerfile](Dockerfile).

FFmpeg is an open-source framework licensed under LGPL and GPL.
See [https://www.ffmpeg.org/legal.html](https://www.ffmpeg.org/legal.html). You are solely responsible
for determining if your use of FFmpeg requires any
additional licenses. CVAT.ai Corporation is not responsible for obtaining any
such licenses, nor liable for any licensing fees due in
connection with your use of FFmpeg.

## Contact us

[Gitter](https://gitter.im/opencv-cvat/public) to ask CVAT usage-related questions.
Typically questions get answered fast by the core team or community. There you can also browse other common questions.

[Discord](https://discord.gg/S6sRHhuQ7K) is the place to also ask questions or discuss any other stuff related to CVAT.

[LinkedIn](https://www.linkedin.com/company/cvat-ai/) for the company and work-related questions.

[YouTube](https://www.youtube.com/@cvat-ai) to see screencast and tutorials about the CVAT.

[GitHub issues](https://github.com/cvat-ai/cvat/issues) for feature requests or bug reports.
If it's a bug, please add the steps to reproduce it.

[#cvat](https://stackoverflow.com/search?q=%23cvat) tag on StackOverflow is one more way to ask
questions and get our support.

[contact@cvat.ai](mailto:contact+github@cvat.ai) to reach out to us if you need commercial support.

## Links

- [Intel AI blog: New Computer Vision Tool Accelerates Annotation of Digital Images and Video](https://www.intel.ai/introducing-cvat)
- [Intel Software: Computer Vision Annotation Tool: A Universal Approach to Data Annotation](https://software.intel.com/en-us/articles/computer-vision-annotation-tool-a-universal-approach-to-data-annotation)
- [VentureBeat: Intel open-sources CVAT, a toolkit for data labeling](https://venturebeat.com/2019/03/05/intel-open-sources-cvat-a-toolkit-for-data-labeling/)

  <!-- prettier-ignore-start -->
  <!-- Badges -->

[docker-server-pulls-img]: https://img.shields.io/docker/pulls/cvat/server.svg?style=flat-square&label=server%20pulls
[docker-server-image-url]: https://hub.docker.com/r/cvat/server
[docker-ui-pulls-img]: https://img.shields.io/docker/pulls/cvat/ui.svg?style=flat-square&label=UI%20pulls
[docker-ui-image-url]: https://hub.docker.com/r/cvat/ui
[ci-img]: https://github.com/opencv/cvat/workflows/CI/badge.svg?branch=develop
[ci-url]: https://github.com/opencv/cvat/actions
[gitter-img]: https://img.shields.io/gitter/room/opencv-cvat/public?style=flat
[gitter-url]: https://gitter.im/opencv-cvat
[coverage-img]: https://coveralls.io/repos/github/cvat-ai/cvat/badge.svg?branch=develop
[coverage-url]: https://coveralls.io/github/cvat-ai/cvat?branch=develop
[doi-img]: https://zenodo.org/badge/139156354.svg
[doi-url]: https://zenodo.org/badge/latestdoi/139156354
[discord-img]: https://img.shields.io/discord/1000789942802337834?label=discord
[discord-url]: https://discord.gg/fNR3eXfk6C
