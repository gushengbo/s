# 训练步骤
1. 创建环境,记得用cuda10.0版本
 
   conda create -n yourname python=3.7

   conda install pytorch==1.2.0 torchvision==0.4.0 cudatoolkit=10.0 -c pytorch
   
   pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

2.训练

   cd models/asl/
   
   python train.py --train-data cub --test-data cub --backbone resnet12 --num-shots 1 --batch-tasks 1 --train-tasks 60000 --semantic-type class_attributes --testonly False

3.测试

   python train.py --train-data cub --test-data cub --backbone resnet12 --num-shots 1 --batch-tasks 1 --train-tasks 60000 --semantic-type class_attributes --testonly True --resume --resume-folder {checkpoint_path}

  
