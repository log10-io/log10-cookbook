# log10-cookbook

`examples/` Examples and guides for using Log10

## Colab notebooks 

In these notebooks, we will build a simple AutoFeedback model with ~20 examples and use it to scale human feedback.

* [How to use Log10 for accuracy improvement using the OpenAI Fine-tuning API](https://colab.research.google.com/drive/1VLT1lXimYWbsmgV85etqALaZbaoIbrRj?usp=sharing):  We'll use the scaled feedback to fine-tune a base model to improve the accuracy of our LLM application

* [How to use Log10 for accuracy improvement using DSPy for automated prompt optimization](https://colab.research.google.com/drive/1obuS9cEWN9MT-MIv5aL1sDIYuGZEKo4r?usp=sharing): We'll use the scaled feedback to use DSPy's automated prompt optimizers to improve the accuracy of our LLM application

[Intro to Log10 AutoFeedback](https://colab.research.google.com/drive/1dVXv56ld6L8k0rVB133tCOguNiRnIlMY?usp=sharing): Build a custom evaluation model (AutoFeedback) for summary grading. Walks through the flow of creating Feedback (via API or GUI), creating an AutoFeedback model (locally or in the cloud), and running inference on the AutoFeedback model on new LLM calls.


## In above tutorials, you will learn how to

1. Use Log10 AutoFeedback to scale human review of LLM outputs (for online monitoring and alerting, or for offline dataset curation for evals, fine-tuning or prompt improvement)
2. Use Log10 AutoFeedback to curate a fine-tuning (or prompt optimization) dataset and drive accuracy improvements

An exciting extrapolation of this approach is the idea of self-improvement by alternating improvements in accuracy of base models and AutoFeedback models -- a self-improving AutoFeedback model (with dynamically selected few-shot examples, the superset of which increase over time) was used to curate data to fine-tune (or prompt optimize) the base model, and assess its accuracy improvement. As more data comes in to the AI application, AutoFeedback helps filter the high quality examples that are most likely to yield accuracy improvements.

Alternatively, both positive and negative (or high and low score) examples could be used to fine-tune using approaches such as DPO (or RLHF)
