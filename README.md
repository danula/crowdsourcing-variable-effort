# The Challenge of Variable Effort Crowdsourcing and How Visible Gold Can Help

This repository provides a refined dataset for evaluating variable effort in crowdsourcing. 

The given annotations were used as ground truth in the CSCW 2021 Paper - The Challenge of Variable Effort Crowdsourcing and How Visible Gold Can Help.

### Selection process

We selected 140 images and ground truth data from the [Open Images dataset](https://storage.googleapis.com/openimages/web/index.html). The number
of faces in the images we selected ranged from 1 to 14, with 10 images per face count. For each
subset, we sorted images by ID and picked the first 10 images corresponding to a pseudo-random
selection. Images with potentially ambiguous human faces, such as cartoon characters or statues,
were excluded to allow for definitive quality assessments. Selected annotations have been further refined and quality checked.

### Data Format

The file `ground-truth-HumanFace140.csv` includes ground truth annotations for 140 images with the following columns.

- image_id (corresponds to Open Images ids)
- label
- n_labels (ranges from 1 to 14)
- ground-truth (For example, in the following format)


    {
        'annotations': 
            [
                {
                    'class_id': 0, 
                    'height': 123.65715, 
                    'width': 92.80000000000001, 
                    'left': 365.44, 
                    'top': 145.442118
                }
            ], 
        'image_size': 
            {
                'height': 683, 
                'width': 1024
            }
    }

You can also download the images from the following public S3 bucket.

https://danula-task-decomposition.s3-us-west-2.amazonaws.com/images/<image_id>.jpg


Please cite the following paper if you are using this dataset. For any questions, refer to the paper or contact the authors.

> D. Hettiachchi, M. Schaekermann, T. McKinney, M. Lease (2021). The Challenge of Variable Effort Crowdsourcing and How Visible Gold Can Help. Proceedings of the ACM on Human-Computer Interaction, 5 (CSCW2), 332:1-332:26. https://doi.org/10.1145/3476073