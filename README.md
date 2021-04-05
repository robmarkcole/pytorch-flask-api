# PyTorch Flask API

This repo contains a sample code to show how to create a Flask API server by deploying our PyTorch model

If you'd like to learn how to deploy to Heroku, then check [this repo](https://github.com/avinassh/pytorch-flask-api-heroku).


## How to 
Install the dependencies:
* `python3 -m venv venv`
* `source venv/bin/activate`
* `pip install -r requirements.txt`

Run the Flask server:

    FLASK_ENV=development FLASK_APP=app.py flask run


From another tab, send the image file in a request:

```
curl -X POST -F file=@hummingbird.jpg http://localhost:5000/predict

{
  "class_id": "n01833805", 
  "class_name": "hummingbird"
}
```

Run successfully on:
```
torch==1.8.1
torchvision==0.9.1
Flask==1.1.2
```


## License

The mighty MIT license. Please check `LICENSE` for more details.
