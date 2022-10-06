# Train a bird classifier
For this model I closely followed the simple process of [Lesson 2](https://course.fast.ai/Lessons/lesson2.html) of the 2022 fastai [Practical Deep Learning for Coders](https://course.fast.ai) course.

The data I used for training comes from this kaggle dataset: [🐦 Singer Bird Species](https://www.kaggle.com/datasets/eisgandar/singer-birds)

The model is released as an app on [huggingface spaces](https://huggingface.co/spaces/benkarr/bird-classifier) using a `convnext_base` and as a [web app](https://ben-karr.github.io/react-bird-classifier) consuming a FastAPI on heroku, using a `resnet18`. The smaller model on heroku was necessary due to limited storage, but the hit in accuracy is acceptable for the conciderable smaller model. (`resnet18`: 47MB | 96.3% acc.; `convnext_base`: 355MB | 98.9% acc.)