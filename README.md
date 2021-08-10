## Skipattn_depth_estimation


## Docker Setting 

- 도커 이미지가 없을 경우
```
make docker-build
```
- 도커 컨테이너 생성 및 실행 (이때 checkpoint가 전체 폴더에 포함되면 도커 컨테이너 용량에 포함이 됨 .. 조심)
```
make docker-start-interactive
```
- cuda 버전이 11일 경우 [참조](https://github.com/pytorch/pytorch/issues/31285#issuecomment-787582949)
```
pip3 install --pre torch torchvision -f https://download.pytorch.org/whl/nightly/cu111/torch_nightly.html -U
```
- horovod 가 없을 경우
```
pip install horovod 
```
- wandb 가 안될 경우
```
pip install wandb --upgrade 
```
- Swin pretrain model download [참조](https://github.com/SwinTransformer/Swin-Transformer-Semantic-Segmentation)
```
wget https://github.com/SwinTransformer/storage/releases/download/v1.0.1/upernet_swin_base_patch4_window7_512x512.pth
```

## training

- train_kitti.yaml 파일을 변경해서 데이터 경로 변경 ! 

```
python3 scripts/train.py configs/train_kitti.yaml
```

## Eval

- [pretrain weight](https://drive.google.com/file/d/1LBz4vQLkLWGVGc1jQSa7Te4xAI3pko6S/view?usp=sharing)
