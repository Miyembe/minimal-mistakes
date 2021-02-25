I was training OpenAI gym BipedalWalker-v3 with PyTorch. 

When I ran the script, CUBLAS_STATUS_EXECUTION_FAILED when calling 'cublasSgemm' error came up.

I checked my CUDA version and found it is 11.2. Also checked CUDNN, it was fine. 

The problem was I had wrong PyTorch. I needed to have torch that is available for cuda 11.0+. 

After reinstalling torch and vision and audio as below, the problem solved. 

'''
pip install torch===1.7.1+cu110 torchvision===0.8.2+cu110 torchaudio===0.7.2 -f
'''

I spent quite long time on reinstalling CUDA, changing symbolic link, etc. 

Hope it helps somebody like me. 
