# 프로젝트 이름
![](https://i.imgur.com/e6t0WFx.png)

## 프로젝트 소개

<p align="justify">
나만의 동숲네컷 만들기<br/>
- 내 사진을 넣어서 동물의 숲에 없는 캐릭터와 함께 네컷사진을 만들자!<br/>
- 내 얼굴과 가장 비슷한 주민을 찾아보자<br/>
</p> 

## 데이터 사용
### [동물의 숲 얼굴 데이터](https://meiker.io/play/11374/online.html)
- 크롤링을 통해 랜덤 얼굴 데이터 수집

### [동물의 숲 주민 데이터](https://animalcrossing.soopoolleaf.com/ko/acna/)
- 랜덤주민 생성을 위해 380개의 동물 주민 데이터 수집

<br>

## 기술 스택

| 언어 | 서비스 플로우 |  문서작업   |  웹구현   |
| :--------: | :--------: | :------: | :-----: |
|   <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">    |  ![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)   | ![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white) | <img src="https://img.shields.io/badge/node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white"> |

<br>

## 서비스 구현

### [서비스 플로우 Figma](https://www.figma.com/proto/GrNnZDseFcYkgxbg45gqXt/%EB%8F%99%EC%88%B2%EB%84%A4%EC%BB%B7?type=design&node-id=1-3&t=Wd2Y4T5OhhIpATnQ-1&scaling=scale-down&page-id=0%3A1&starting-point-node-id=1%3A3&mode=design)
#### 메인 화면
![](https://i.imgur.com/2ZUFpCv.png)
#### 동숲 네컷 프레임 제작
![](https://i.imgur.com/qwsmElf.png)
#### 동숲 네컷 캐릭터 제작
![](https://i.imgur.com/FaFO0t1.png)
#### 동숲 네컷 최종 결과
![](https://i.imgur.com/b8qGYGJ.png)
#### 동숲 닮은 꼴 찾기
![](https://i.imgur.com/mwf8huk.png)
### 플로우 차트
![](https://i.imgur.com/5ZMoRpD.jpg)


<br>

## 구현 기능

### 1.1 인생네컷 프레임 생성
[kohya_ss](https://github.com/bmaltais/kohya_ss)
```
1. kohya_ss 공식 github에서 클론하기
2. 데이터셋을 활용하여 생성한 SDXL-Lora 모델 활용
3. ComfyUI로 인생네컷 프레임 배경 생성
```
**결과**
![](https://i.imgur.com/6SSuL4G.png)
![](https://i.imgur.com/v9aNKWr.png)
![](https://i.imgur.com/WL4nske.png)
![](https://i.imgur.com/pJAzErT.png)

### 1.2 인생네컷 주민 생성
```
1. 주민 얼굴 380개의 데이터셋을 활용하여 Lora 생성
2. ComfyUI로 주민 얼굴 생성
```
**결과**
![](https://i.imgur.com/MOYhTQf.png)
![](https://i.imgur.com/VXnSFNq.png)
![](https://i.imgur.com/TgyjAz2.png)
![](https://i.imgur.com/3dGrjPk.png)

### 1.3 얼굴 => 캐릭터 변환
```
1. 랜덤 얼굴 생성 페이지에서 랜덤한 얼굴 생성 크롤링
2. 얼굴만 활용하기 위해서 배경 제거
3. Lora 생성 후 Stable Diffusion을 사용해 얼굴 변환
4. api 생성해서 웹에서 호출
```
**결과**
![Input 이미지](https://i.imgur.com/O9Fwp2K.png)
![Output 이미지1](https://i.imgur.com/GOohflh.png)
![Output 이미지2](https://i.imgur.com/Xbx8oe1.png)
![Output 이미지3](https://i.imgur.com/UQjw9M1.png)
![Output 이미지4](https://i.imgur.com/HAv0tkY.png)

### 2.1 닮은 꼴 찾기
```
1. ViT를 이용하여 AutoEncoder 구조로 인코더와 디코더 둘 다 주민 이미지를 넣어서 학습
2. faiss 알고리즘을 활용하여 닮은 꼴 찾기 생성
3. huggingface에 있는 pipeline함수를 이용해서 gradio로 웹 api 구현
```
![Input 이미지](https://i.imgur.com/VtPdTpK.png)
![Output 이미지](https://i.imgur.com/nMNc8Qu.png)


### [웹페이지 구현](https://animal-forest-smoky.vercel.app/)
```
Next.js를 통해 구현
```


<br>

## 개선사항

<p align="justify">

</p>

1. api 호출 문제 개선을 통해 기획한 대로 웹페이지 전체 구현
2. 적합한 모델을 찾기 위한 추가 리서치 필요
3. 모델들을 하나로 병합하여 멀티모달 서비스 구축

<br>

## 라이센스

MIT &copy; [NoHack](mailto:lbjp114@gmail.com)

<!-- Stack Icon Refernces -->

[js]: /images/stack/javascript.svg
[ts]: /images/stack/typescript.svg
[react]: /images/stack/react.svg
[node]: /images/stack/node.svg




<br>

