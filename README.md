I created an image-classification model using Google’s Teachable Machine to recognize several common desk objects. I trained multiple classes with webcam images, tested and refined the model, and then exported the final version to GitHub along with a reflection on its performance, challenges, and limitations.

The objects my model was trained to identify:
* Class 1 (Hair Claw Clip)
* Class 2 (Pen)
* Class 3 (AirPods Case)

* 1.  **Model Performance & Iteration:**
    * My initial trained model demonstrated partial accuracy. While it successfully recognized the hair claw clip, it struggled to correctly identify the pen and the AirPods case. 
    * To improve the model’s performance, I added additional photos and incorporated more diverse images with slightly varied backgrounds.
    * These changes significantly improved the model’s accuracy and confidence scores, as its predictions became more reliable with each additional set of images.

2.  **Challenges & Observations:**
    * The hair claw clip was the easiest object for my model to learn and distinguish. This is likely because it has a very distinct shape and outline compared to the other objects, making its visual features easier for the model to recognize consistently across different images.
    * The pen and the AirPods case were the most challenging objects for the model to recognize. Their simpler shapes and more subtle visual features made them harder to distinguish, especially when photographed against different angles or backgrounds.
    * When I showed the model an object it wasn’t trained on, the confidence bars fluctuated wildly as it tried to force the unknown object into one of the existing classes. This behavior is significant because it shows that the model lacks a true “unknown” category and will always attempt to classify unfamiliar items, highlighting a common limitation in simple image-classification models and the importance of diverse, representative training data.

3.  **Bias in AI:**
    * If I only trained my “Hair Claw Clip” class using images of my specific black claw clip, the model likely would not recognize another student’s claw clip that differs in color, size, or shape. This demonstrates how bias can be introduced through training data, because the model learns only from the limited examples it sees and therefore develops a narrow understanding of what that object looks like, reducing its ability to generalize to real-world variations.
    * If all of my training images were taken in very bright, direct lighting, the model would likely struggle to recognize objects in dim lighting or in areas with strong shadows. This happens because the model becomes overly dependent on the lighting conditions it was trained on, revealing how limited training environments can create biases and reduce the model’s reliability when used in real world situations with different visual conditions.

4.  **Model Limitations & Usefulness:**
    * Some key limitations of my model include its difficulty recognizing objects with similar shapes, its sensitivity to lighting changes, and its limited ability to generalize beyond the specific examples it was trained on. Because the dataset was small and not highly diverse, the model can misclassify unfamiliar versions of the same object or struggle with backgrounds and angles it hasn’t seen before.
    * Being able to download and share the trained model files, such as model.json and weights.bin, is useful because it allows the model to be reused, tested, or deployed outside of Teachable Machine. Sharing these files on platforms like GitHub enables collaboration, version control, and integration into real applications, making it possible for others to run the model, build on it, or use it in their own projects.

5.  **Real-World Applications & Ethics:**
    * A few real-world applications where a similar image classification model could be useful include, Inventory Managment, Security and Access Control and Quality Control Manefacturing. Inventory Management: A model could automatically identify items on store shelves to track stock levels or detect when products need restocking. Security & Access Control, Image classification could help recognize authorized badges or equipment, improving workplace or school security systems. Quality Control in Manufacturing, A model could detect defective parts or products on an assembly line by comparing them to correct examples.
    * One important ethical consideration is privacy. Developers must ensure that image recognition systems do not unintentionally collect or analyze sensitive personal information without consent, as misuse of visual data can lead to surveillance concerns, loss of autonomy, or violations of individual rights.
