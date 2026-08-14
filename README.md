# Urdu OCR Project

## Research Summary

### What is OCR?
OCR (Optical Character Recognition) is a technology that converts text from images into editable digital text. It helps computers read printed or handwritten documents. OCR saves time and reduces manual typing.

### Why is Urdu OCR harder than English OCR?
Urdu OCR is harder because Urdu is written from right to left. Many letters change their shape depending on their position in a word. Urdu also has connected letters and dots, making recognition more difficult.

### Real-world Uses of Urdu OCR
1. Digitizing old Urdu books, newspapers, and historical documents.
2. Converting scanned Urdu forms and government records into editable digital text.
3.
4.
   ## Why We Need a Better Model

  Gap Analysis
Image 1

Actual Urdu Text:
(فیصلوں کی وجہ سے ہوا۔ کراچی کے نرسلا وار میں
سفید پوش لوگوں کے گھر اور قیمتی تھے جن سے
انہیں محروم کر دیا گیا، فیصلے کرنے والے اُس
وقت کے جج جانے کس تذبذب میں تھے۔ وہ
فیصلہ کر کے چلتے گئے۔ اب اُن کا فیصلہ کالعدم
تو ہو گیا ہے مگر اس نقصان کا ازالہ کیسے ہوگا جو ہو
چکا ہے۔ اتنے بڑے فیصلے کس آسانی سے کر)

Tesseract Output:
The OCR recognized some Urdu words, but many characters were incorrect and several words were not recognized properly.

What went wrong?
The output contained incorrect characters, missing words, and spelling mistakes. Although some words were readable, the sentence was not completely accurate.

Image 2

Actual Urdu Text:
(بنائی گئی اور وہ درخت بچا لیے گئے۔ ہمارے
ہاں اول تو درختوں کے قتلِ عام کا کوئی نوٹس
نہیں لیا جاتا، لاہور جیسے شہر میں بھی سگنل انڈر
پاس جان کی سڑک کو بنانے کے لیے گھنے اور پرانے
درختوں کے گلے کاٹ دیتے ہیں۔ یہ بھی کہا
جاتا ہے درخت ہی تو ہیں اور لگا دیں گے اور لگا
دیں گے۔ صاحب! یہ بات تو ہضم ہوتی رہی ہے
مگر یہ ہی ڈھائی ایسے لوگ کیا سوچیں گے کہ وہ مجبوروں کو
اجاڑنے کا منصوبہ لے آئے۔ ہمارے ایک پروفیسر)

Tesseract Output:
No text was detected.

What went wrong?
Tesseract failed to recognize the Urdu text. It returned an empty result even though the image contained clear text.

Image 3

Actual Urdu Text:
(کے من میں آ جانے کے کر گزرتے ہیں۔ اُس وقت
انہیں پوچھنے والا کوئی نہیں ہوتا، ہاں آگے چل کر
وہ اگر تاریخ کے نہر چہرے میں آ جائیں تو تاریخ یہ
فیصلہ کرتی ہے کہ انہوں نے اچھا کام کیا یا
بُرے ظلم کے مرتکب ہوئے۔ اس حوالے سے
حالیہ دنوں میں دو مثالیں سامنے آئی ہیں۔
وفاقی آئینی عدالت نے کراچی کے نسلہ ٹاور اور
اسلام آباد کے منال ریسٹورنٹ کو گرانے والے)

Tesseract Output:
No text was detected.

What went wrong?
The OCR engine could not identify any Urdu characters. The output was completely blank.

Image 4

Actual Urdu Text:
(میں اور وینکوور میں زندگی گزار چکے ہیں۔ اس لیے
انہیں یہ بات بجا نظر آ رہی ہے۔ انہوں نے
ایک واقعہ سنایا کہ وینکوور میں ایک سڑک بننا
تھی، مگر اس سڑک پر پینتیس کے دو بڑے درخت
راستے میں آتے تھے، وہاں جب یہ تجویز آئی کہ
ان درختوں کو کاٹ دیا جائے تو ایک طوفان برپا
ہو گیا۔ لوگوں کی حد درجے مخالفت کے بعد ان)

Tesseract Output:
The OCR extracted some Urdu text, but many words were incorrect and several characters were replaced with the wrong ones.

What went wrong?
Many characters were misrecognized, causing incorrect words and making the sentence difficult to understand. Some parts of the text were also missing.

Image 5

Actual Urdu Text:
(کے جانے ہی اس مکان کو دفنا دیا جاتا ہے کیونکہ
یہ کسی اور کو رہنے پر نہیں دیا جا سکتا، اس کا
آخری ٹھکانہ قبر ہوتی ہے۔ بہرحال سے ایسے یومِ حشر
اٹھایا جائے گا۔ میں نے ایک دو ویڈیوز بھی
میں جن میں ہی دیکھی، ان کے ابا قبروں کے
کتبے اور تعویز اُکھاڑ کر دوسری جگہ لے جا رہے
ہیں کیا قبر صرف ایک سنگ و خشت کا بہانہ
ہوتی ہے؟ جس کا پتھر اُکھاڑ کر جہاں چاہو لگا دو۔ یہ)

Tesseract Output:
The OCR recognized part of the text, but several words contained errors and the sentence was incomplete.

What went wrong?
The recognition accuracy was low. Some words were identified correctly, while others were incorrect or missing, reducing the overall readability.

Summary:

Tesseract fails on Urdu because Urdu is a connected cursive script with complex character shapes and many letters that look similar. During testing, some images produced blank results, while others contained incorrect characters, missing words, and inaccurate sentences. These errors make the extracted text unreliable for real-world use. Therefore, a more advanced OCR model is needed to recognize Urdu text with higher accuracy and consistency.




# Urdu OCR — Fine-Tuned TrOCR Model

A fine-tuned TrOCR model for extracting Urdu text from images using a custom Urdu OCR dataset.

## 1. Project Title and One-Line Description

**Urdu OCR — Fine-Tuned TrOCR Model**

This project uses a fine-tuned TrOCR (Transformer-based Optical Character Recognition) model to recognize and extract Urdu text from images.

---

## 2. What Problem This Solves and Why It Matters

Optical Character Recognition (OCR) is used to convert text present in images into editable digital text. However, Urdu OCR is more challenging than English OCR because Urdu is written from right to left, contains connected characters, and the shape of characters can change depending on their position in a word.

Traditional OCR systems may produce incorrect or incomplete Urdu text, especially when images contain different fonts, sizes, backgrounds, or image quality.

This project aims to improve Urdu text recognition by fine-tuning a TrOCR model on a custom Urdu image dataset.

### Real-World Use Case

An Urdu OCR system can be useful for digitizing Urdu books, documents, newspapers, handwritten or printed Urdu material, and historical documents. It can convert Urdu text from images into searchable and editable digital text, saving time and reducing manual typing.

---

## 3. How It Works

This project uses **TrOCR (Transformer-based Optical Character Recognition)**.

TrOCR is a deep learning model designed to recognize text from images. The model receives an image containing text and predicts the corresponding text.

### Basic Workflow

```text
Urdu Text Image
       ↓
Image Preprocessing
       ↓
TrOCR Processor
       ↓
Fine-Tuned TrOCR Model
       ↓
Predicted Urdu Text
```

### What Fine-Tuning Means

Fine-tuning means taking a model that has already learned general text-recognition patterns and training it further on our own Urdu dataset.

Instead of training a complete OCR model from the beginning, we provide Urdu images together with their correct Urdu text labels. The model learns the relationship between the Urdu images and their corresponding text.

### How Our Dataset Fits In

Our custom dataset contains Urdu text images along with their correct text labels. These image-text pairs are used to fine-tune the TrOCR model so that it becomes better suited for Urdu text recognition.

---

## 4. Live Demo

The trained model/application can be tested through the Hugging Face Space.

**Hugging Face Space:**
https://huggingface.co/kashaf112-s/SI26-urdu-ocr-model-kashaf

Example:

```text
https://huggingface.co/spaces/kashaf112-s/SI26-urdu-ocr-model-kashaf
```

---

How to Run It Locally

Follow these steps to run the Urdu OCR project on your local computer.

Step 1 — Clone the Repository

First, clone the GitHub repository:

git clone https://github.com/kashaf11303/urdu-ocr-codesaviours-si26-kashaf

Then move into the project folder:

cd urdu-ocr-codesaviours-si26-kashaf
Step 2 — Install Required Libraries

Make sure Python is installed on your computer.

Install the required dependencies using:

pip install -r requirements.txt
Step 3 — Run the Streamlit Application

Start the Streamlit application using:

streamlit run app.py

After running this command, Streamlit will provide a local URL in the terminal, usually:

http://localhost:8501

Open this URL in your web browser.

Step 4 — Upload an Urdu Image

Upload an image containing Urdu text through the Streamlit application.

The application will process the image using the fine-tuned TrOCR model and display the predicted Urdu text.

Requirements
Python 3.x
PyTorch
Hugging Face Transformers
Pillow
Streamlit
OpenCV
Internet connection for downloading required model/dependencies

## 6. Dataset Details

A custom dataset was prepared for this Urdu OCR project.

### Dataset Information

* **Number of images:** 200
* **Text language:** Urdu
* **Task:** Urdu Optical Character Recognition
* **Image type:** Urdu text images
* **Labels:** Corresponding Urdu text for each image
* **Model:** TrOCR
* **Training:** Fine-tuning on the custom Urdu dataset

### Dataset Variety

The dataset was collected with variation in:

* Different Urdu text styles
* Different font sizes
* Different fonts
* Different image sizes
* Different backgrounds
* Different text layouts

The purpose of using variation in the dataset was to help the model recognize Urdu text under different visual conditions.

### Preprocessing

The images were preprocessed before being provided to the model. Preprocessing included operations such as:

* Converting images to a suitable format
* Resizing images
* Grayscale conversion where required
* Noise reduction
* Thresholding where required

These steps help prepare the images for OCR processing.

---

## 7. Results

The fine-tuned TrOCR model was evaluated on Urdu text images.

### Accuracy

**Model Accuracy: 0.0% **

The model was able to recognize Urdu text from the test images, but the performance can still be improved.

Because the dataset contains a relatively small number of images, the model may not generalize perfectly to completely new Urdu fonts, backgrounds, image qualities, and text styles.

### Future Improvements

With more time and resources, the following improvements could be made:

1. Increase the size of the Urdu OCR dataset.
2. Collect images using more Urdu fonts.
3. Add more background variations.
4. Include different image resolutions and text sizes.
5. Increase the number of training epochs carefully.
6. Use data augmentation to create more training variations.
7. Collect more diverse Urdu text samples.
8. Evaluate the model using a larger and completely unseen test dataset.

A larger and more diverse dataset would likely help the model perform better on real-world Urdu documents.

---

## 8. Technologies Used

* Python
* PyTorch
* Hugging Face Transformers
* TrOCR
* PIL/Pillow
* OpenCV
* Streamlit
* Google Colab
* Hugging Face Spaces

---

## 9. Project Structure

```text
Project Structure
Urdu-OCR/
│
├── 📄 app.py
├── 📄 requirements.txt
├── 📄 README.md
├── 📄 labels.csv
│
├── 📁 200 images/
│   ├── 🖼️ image1.jpg
│   ├── 🖼️ image2.jpg
│   ├── 🖼️ image3.jpg
│   ├── 🖼️ image4.jpg
│   └── 🖼️ ...
│
├── 📁 model/
│   ├── 📄 config.json
│   ├── 📄 preprocessor_config.json
│   ├── 📄 tokenizer_config.json
│   ├── 📄 special_tokens_map.json
│   ├── 📄 tokenizer.json
│   ├── 📄 vocab.json
│   └── 📄 model files
│
└── 📁 preprocessing/
    └── 📄 preprocessing.py
## 10. Credit

**Built during the Code Saviours ML/AI Internship — Batch SI-26.**

**Name:** [Hafiza Kashaf Shahzad]

---

## 11. Conclusion

This project demonstrates the use of a fine-tuned TrOCR model for Urdu Optical Character Recognition. A custom Urdu dataset was prepared and used to fine-tune the model for recognizing Urdu text from images.

The project shows how transformer-based OCR models can be adapted for languages such as Urdu. Although the current results can be improved, especially with a larger and more diverse dataset, this project provides a foundation for building more accurate Urdu OCR systems for real-world applications.

