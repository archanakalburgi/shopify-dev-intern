# Plan
Store all the image feature in to annoy tree and save the file on to the disk. 
![wd](plan.svg)


## Implementation Plan
### V1
- [x] Make sure the plan is doable MVP (in ipynb)
    - [x] Annoy tree store and retrive - done
    - [x] Image feature extraction - done
    - [x] Image search is it any good? - Good, as far as we have good amount of images indexed
- [x] Back End - (Using flask)
    - [x] API to search - Building a react app would be nice, but tome consuming. So using Flask Views
    - [x] API to upload image for search - Done
    - [X] API to add images to repo(may be) - 
            Images can be uploaded by the user to index. But index is batch based, would need be done by the user. In future we can add a airflow job to run every hour to keep the index updated. 
- [x] Front End - (Using boot strap)
    - [x] Grid of images limit to 16 images a page
    - [x] Search text box
    - [x] Search image box 
    - [ ] Make it look like, an adult made it. 
- [x] Deployment 
    - [x] local server setup instructions
    - [x] DockerFile so that it is easy to get the application running.
    - [x] Heroku deployment - deployed to digital ocean instead of heroku

### V2
- [ ] Automate index creation when new images are added to the repo.
- [ ] Use fast API to get, so that API can be used by other projects
- [ ] React App would be nice.
- [ ] Host all image assets on GCS or Digital Ocean Storage  - Will also reduce the image size.


## Assumptions
- Should be able to see the work, without any installation.
- Should be able to run the project in 10 min.  - docker or script
- Should be able feel what this project is about without having to get the whole thing running
    - Host it on heroku?
    - Make a docker image? so that it just runs (docker is everywhere?)




# Why annoy 

# Auth is tricy
# Limitations
- Batch based, annoy tree cannot be updated in real time.


# Idead about scaling
Annoy has limitations
Works batchbaed, we might wan to get to real time soon
- https://milvus.io/bootcamp 
