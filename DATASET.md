# Dataset preprocess

Here i will specify how to use GCP and how to generate trainning triplets from MS MARCO Document Ranking dataset.

## Google Cloud Platform (GCP)

Google provide $300 free trial in GCP for 1 year, with this you can make a lot of things since the usage per hour is not that much (just remember to shutdown the machine every time that you are not using!!!)

https://www.cloudbooklet.com/how-to-set-up-jupyter-notebook-on-ubuntu-18-04-in-google-cloud/


## MS MARCO preprocess

GCP is necessary because the documents file of MS MARCO requires 37GB memory to load, so we need a machine with more than this of RAM memory. There is a way to extract tripletes from files without need to load all files, but i tried this in google colab (with is a good machine to us mortals) and to generate 100 tripletes it took me 5 hours so its unfeasible to generate all ~360k tripletes, with the code that i will describe here it took me around **2 hours** to have all possible tripletes.



