# social-distance-detection-using-computer-vision-and-deep-learning 
This project detects the social distance in public, and if the distance between the people is less than the threshold distance, it shows the number of violations in that frame of a video. In this project, there is a comparison between the optimised version that used the Intel OpenVINO toolkit and the unoptimized version without using OpenVINO.
# To run the code file present in social distance with openvino 
1)create a seperate conda environment

2)install OpenVINO toolkit :
>https://www.intel.com/content/www/us/en/developer/tools/openvino-toolkit/download.html?ENVIRONMENT=DEV_TOOLS&OP_SYSTEM=WINDOWS&VERSION=v_2023_0&DISTRIBUTION=PIP

3)download Intel OpenVINO's toolkit pretrained model:
>person-detection-0202,
>This is a person detector that is based on MobileNetV2 backbone with two SSD heads from 1/16 and 1/8 scale feature maps and clustered prior boxes for 512x512 resolution.
>https://docs.openvino.ai/2022.3/omz_tools_downloader.html


4) requirements
>jupyter notebook
>install opencv,
>load the xml and bin files path of pretrained model correctly,
>upload the video path.

# Image of social distance detection with OpenVINO 
1) check the FPS on top left 
2) check the number of violations in the bottom
![Capture](https://github.com/RaviTeja20003/social-distance-detection-using-computer-vision-and-openvino/assets/103447565/59c473c1-2786-47b7-aece-660d893a528f)

# Image of social distance detection witout OpenVINO
1) check the FPS on top left
2) check the number of violations in the bottom
![Capture](https://github.com/RaviTeja20003/social-distance-detection-using-computer-vision-and-openvino/assets/103447565/cf1d2f37-3df5-42e3-8ded-284e84d85216)

# check this output video of social distance detection using OpenVINO

VIDEO LINK:https://youtu.be/IaGS79e84j4

Description:
1)Model used in this video is person-detection-0202,
This is a person detector that is based on MobileNetV2 backbone with two SSD heads from 1/16 and 1/8 scale feature maps and clustered prior boxes for 512x512 resolution. Downloaded from Intel OpenVINO toolkit pretrained models.
2)check the FPS of the video on the left top corner and the number of violations in the bottom,Social distance is measured between people who are close to each other and a red line is drawn in between these people, if the distance between the people is less than the threshold distance then number of violations would be increased  and when two or more people detected at a time in a frame less than the threshold distance then each pair would be taken into count so, there might be an increase in repetitive count of number of violations only in this case .As OpenVINO toolkit is used the FPS of the video has increased 8 times when compared with the model that has not used OpenVINO.

# check this output video of social distance detection without using OpenVINO

VIDEO LINK:https://youtu.be/KT_DkvnSgmY

Description:
1)Model used in this video is yoloV3 weights and cfg files
2)People who violate social distance are detected with red colored boxes as these people are less than the threshold distance and all the remaining people are detected in the green boxes.



