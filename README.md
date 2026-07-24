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

