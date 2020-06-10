# Training pipeline

Here i will specify how to use GCP and how to effectivelly train an Document Ranking Model with MS MARCO.

## Google Cloud Platform (GCP)

Differently from dataset preprocess here i needed GPU instance, so for this we need to signup on GCP (instead of using just the free trial), but relax the $300 keep in your account so just don't let your usage to pass this values. GPU requires more $ per hour of running so be extremely careful on turn off your VM. So next step is to solicite an "ALL REGIONS" GPU quota. After that you will be able to initiate and GPU VM. Particulally i have some problems to instantiate an V100 GPU VM so i worked with a T4.

https://cloud.google.com/ai-platform/deep-learning-vm/docs/pytorch_start_instance

## Long Sentences Transformers

We use Reformer and LongFormer to model our IR-Model
