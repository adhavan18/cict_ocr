<h1 align="center"> CICT_OCR, An Easy,  - (ஒளி எழுத்துணரி)</h1>

<p align="center">❤️️❤️️Please star✨ it if you like❤️️❤️️</p>

<p align="center">
  <a href="LICENSE">
    <img src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/MIT.svg" alt="LICENSE">
  </a>
  <a href="">
    <img src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/huggingface.svg" alt="HuggingSpace">
  </a>
   <a href="">
    <img src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/colab.svg" alt="colab">
  </a>
</p>


<div align="center">
  <p>
    <a href="https://github.com/adhavan18/cict_ocr">
    <img width="50%" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/logo_1.gif">
    </a>
  </p>
</div>

 CICT-OCR, We from the Central Insitute of Classical Tamil have developed this apart from other ocr modules available, helps you recognise old-tamil manuscripts with high accuracy. This OCR is much more robust to tilted text compared to the Tesseract, Easy OCR and ocr_tamil as they are primarily built to work on the documents texts and not on manuscripts

## Languages Supported 🔛
**➡️ English**

**➡️ Tamil (தமிழ்)**

## Accuracy 🎯
✔️ English > 98%

✔️ Tamil > 95%

## Comparison between Tesseract OCR, EasyOCR and OCR Tamil ⚖️

🏎️ *10-40% faster inference time than EasyOCR and Tesseract*

 Input Image                                                                |  OCR TAMIL   🏆         | Tesseract         | EasyOCR |
|:--------------------------------------------------------------------------:|:--------------------:|:-----------------:|:-----------------:|
| <img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/4.jpg">                   | வாழ்கவளமுடன்✅     |    க்‌ க்கஸாரகளள௮ஊகஎளமுடன்‌ ❌  | வாழக வளமுடன்❌|
| <img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/11.jpg">                   | தமிழ்வாழ்க✅      | **NO OUTPUT** ❌           | தமிழ்வாழ்க✅      |
| <img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/2.jpg">                   | கோபி ✅              | **NO OUTPUT** ❌          | ப99❌          |
| <img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/6.jpg">                   | தாம்பரம் ✅           | **NO OUTPUT** ❌ | தாம்பரம❌ |
| <img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/1.jpg">                   | நெடுஞ்சாலைத் ✅      | **NO OUTPUT** ❌             |நெடுஞ்சாலைத் ✅      |
| <img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/5.jpg">                   | அண்ணாசாலை ✅     | **NO OUTPUT** ❌            |  ல@I9❌            |
| <img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/10.jpg">                  | ரெடிமேட்ஸ் ✅         |**NO OUTPUT** ❌     | ரெடிமேடஸ் ❌         |

**Obtained Tesseract and EasyOCR results using the [Colab notebook](https://colab.research.google.com/drive/1ylZm6afur85Pe6I10N2_tzuBFl2VIxkW?usp=sharing) with Tamil and english as language**

## Handwritten Text (Experimental)🧪
<img width="500" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/develop/test_images/tamil_handwritten.jpg">


```
MODEL OUTPUT: நிமிர்ந்த நன்னடை மேற்கொண்ட பார்வையும் 
நிலத்தில் யார்க் கும் அஞ்சாத நெறிகளும் 
திமிர்ந்த ஞானச் செருக்கும் இருப்பதால் 
செம்மை மாதர் திறம்புவ தில்லையாம் 
அமிழ்ந்து பேரிரு ளாமறி யாமையில் 
அவல மெய்திக் கலையின்  வாழ்வதை 
உமிழ்ந்து தள்ளுதல் பெண்ணற மாகுமாம் 
உதய கன்ன உரைப்பது கேட்டிரோ 
பாரதியார் 
ஹேமந்த் ம 
```


## How to Install and Use OCR Tamil 👨🏼‍💻

### Quick links🌐
📔 Detailed explanation on [Medium article](https://gnana70.medium.com/ocr-tamil-easy-accurate-and-simple-to-use-tamil-ocr-b03b98697f7b). 

✍️ Experiment in [Colab notebook](https://colab.research.google.com/drive/11QPPj3EmpoIqnpuIznKeP1icxvVOjfux?usp=sharing)

🤗 Test it in [Huggingface spaces](https://huggingface.co/spaces/GnanaPrasath/cict_ocr)


### Pip install instructions🐍
In your command line, run the following command ```pip install cict_ocr```

If you are using jupyter notebook , install like ```!pip install cict_ocr```

### Python Usage - Single image inference

**Text Recognition only**

```python
from cict_ocr.ocr import OCR

image_path = r"test_images\1.jpg" # insert your own path here
ocr = OCR()
text_list = ocr.predict(image_path)
print(text_list[0])

## OUTPUT : நெடுஞ்சாலைத்
```
<img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/1_180.jpg">


**Text Detect + Recognition**

```python
from cict_ocr.ocr import OCR

image_path = r"test_images\0.jpg" # insert your own image path here
ocr = OCR(detect=True)
texts = ocr.predict(image_path)
print(" ".join(texts))

## OUTPUT : கொடைக்கானல் Kodaikanal 

```
<img width="400" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/0.jpg">


### Batch inference mode 💻

**Text Recognition only**

```python
from cict_ocr.ocr import OCR

image_path = [r"test_images\1.jpg",r"test_images\2.jpg"] # insert your own image paths here
ocr = OCR()
text_list = ocr.predict(image_path)

for text in text_list:
    print(text)

## OUTPUT : நெடுஞ்சாலைத்
## OUTPUT : கோபி

```

**Text Detect + Recognition**

```python
from cict_ocr.ocr import OCR

image_path = [r"test_images\0.jpg",r"test_images\tamil_sentence.jpg"] # insert your own image paths here
ocr = OCR(detect=True)
text_list = ocr.predict(image_path)

for item in text_list:
  print(" ".join(item))
    

## OUTPUT : கொடைக்கானல் Kodaikanal 
## OUTPUT : செரியர் யற்கை மூலிகைகளில் இருந்து ஈர்த்தெடுக்க்கப்பட்ட வீரிய உட்பொருட்களை உள்ளடக்கி எந்த இரசாயன சேர்க்கைகளும் இல்லாமல் உருவாக்கப்பட்ட இந்தியாவின் முதல் சித்த தயாரிப்பு 

```

### Advanced usage🚀

OCR module can be initialized by setting following parameters as per your requirements

```
1. Confidence of word ->  OCR(details=1)
2. Bounding Box and Confidence of word -> OCR(detect=True,details=2)
3. To change the CRAFT Text detection settings -> OCR(detect=True,text_threshold=0.5,
                                               link_threshold=0.1,
                                               low_text=0.30)
4. To increase the Batch size of text recognition -> OCR(batch_size=16) # set as per available memory
5. To configure the language to be extracted -> OCR(lang=["tamil"]) # list can take "english" or "tamil" or both. Defaults to both language
```

**Tested using Python 3.10 on Windows & Linux (Ubuntu 22.04) Machines**

## Applications⚡
1. ADAS system navigation based on the signboards + maps (hybrid approach) 🚁
2. License plate recognition 🚘

## Limitations⛔

1. Document text reading capability is not supported as library doesn't have

      **➡️Auto identification of Paragraph**

      **➡️Orientation detection**

      **➡️Skew correction**

      **➡️Reading order prediction**

      **➡️Document unwarping**

      **➡️Optimal Text detection for Document text not available**  

      (**WORKAROUND** Bring your own models for above cases and use with OCR tamil for text recognition)


2. Unable to read the text if they are present in rotated forms

<p align="left">
<img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/9.jpg"> 
<img width="200" alt="teaser" src="https://github.com/adhavan18/cict_ocr/raw/main/test_images/8.jpg">
</p>

3. Currently supports Only Tamil Language. I don't own english model as it's taken from open source implementation of parseq


## Acknowledgements 👏

**Text detection** - [CRAFT TEXT DECTECTION](https://github.com/clovaai/CRAFT-pytorch)

**Text recognition** - [PARSEQ](https://github.com/baudm/parseq)
