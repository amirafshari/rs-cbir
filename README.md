# Content Based Image Retrieval for Satellite Data
<a target="_blank" href="https://colab.research.google.com/github/amirafshari/rs-cbir/blob/main/vision-language-search.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
<a target="_blank" href="https://colab.research.google.com/github/amirafshari/rs-cbir/blob/main/image-search.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
  

With the rapid advancement of remote sensing technologies, the availability of large-scale satellite image datasets has grown exponentially. These datasets contain invaluable information for various applications, including environmental monitoring, urban planning, and disaster management. However, searching for specific categories of objects, such as identifying all images which are similar to a sepcific query (image/text) within a dataset of thousands or millions or even billions of samples, presents a significant challenge for human analyst.  

### Solution
This task, which is overwhelming for human analysts, can be efficiently addressed using vector search techniques. By leveraging deep learning models to transform images into high-dimensional vectors and utilizing various models such as classification, segmentation, etc, we can use their last layer features and employ nearest neighbor search algorithms to quickly and accurately retrieve relevant images based on their content or semantic meaning.  

For instance, you find and interesting shape in your dataset and you want to figure out if there is any similar image in your dataset or not? To do so, you can use that image as a search query to find the similar images.  

Or in a Vision-Language model, you can search for "red ship floating on the ocean" and use it as the query and the system provides you the appropriate instances of the dataset while there is no metadata available.

### Good to know
- We just fine-tuned ResNet50 on AID dataset, we can train more architectures on different datasets and benchmark them.
- By fine-tuning on a large-scale dataset, the accuracy significantly improves.
- It's not a production-level (or even near-production-level) solution, so there is plenty of room for improvement in both speed and accuracy.
- We can use vector databases such as Weaviate or Redis instead of a simple Python list.
- It's good to dig into the datasets first and then judge the performance of the model.


# Results

### Visual Search
**Query: Church (Image)**  

![jpg](results/vision/w-aid-data-aid-church.jpg)
  
**Query: Mountain (Image)**  

![jpg](results/vision/w-aid-data-aid-mountain.jpg)
  
**Query: Parking (Image)**  

![jpg](results/vision/w-aid-data-aid-parking.jpg)
  
**Query: Baseballfield (Image)**  

![jpg](results/vision/w-aid-data-aid-baseballfield.jpg)



### Vision Language (Multimodal)
**Query: Stadium (Text)**  

![jpg](results/vision-language/stadium.jpg)