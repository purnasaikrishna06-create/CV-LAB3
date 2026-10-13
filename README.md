# CV-LAB3
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("/content/images (2).jpg")

img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

avg_3x3 = cv2.blur(img, (3, 3))
avg_5x5 = cv2.blur(img, (5, 5))
avg_7x7 = cv2.blur(img, (7, 7))

avg_3x3_rgb = cv2.cvtColor(avg_3x3, cv2.COLOR_BGR2RGB)
avg_5x5_rgb = cv2.cvtColor(avg_5x5, cv2.COLOR_BGR2RGB)
avg_7x7_rgb = cv2.cvtColor(avg_7x7, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(12, 8))

plt.subplot(2, 2, 1)
plt.imshow(img_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(2, 2, 2)
plt.imshow(avg_3x3_rgb)
plt.title("Average Filter 3x3")
plt.axis("off")

plt.subplot(2, 2, 3)
plt.imshow(avg_5x5_rgb)
plt.title("Average Filter 5x5")
plt.axis("off")

plt.subplot(2, 2, 4)
plt.imshow(avg_7x7_rgb)
plt.title("Average Filter 7x7")
plt.axis("off")

plt.tight_layout()
plt.show()
