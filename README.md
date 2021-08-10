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
## training

- train_kitti.yaml 파일을 변경해서 데이터 경로 변경 ! 

```
python3 scripts/train.py configs/train_kitti.yaml
```

