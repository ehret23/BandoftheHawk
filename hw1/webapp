import time
import redis 
from flask import Flask 
from flask import request 
from flask import Response
import requests


app = Flask(__name__)
cache = redis.Redis(host='redis', port=6379)

@app.route('/')
def standby():
	return 'bitchin'


@app.route('/hello')				 
def Hello():
	if request.method == "GET":		
        	
		return 'Hello world!'

	elif request.method == "POST":		
		
		return 'status code 405'


@app.route('/test', methods = ['GET', 'POST', 'PATCH', 'PUT', 'DELETE'])									
def Test():
	if request.method == 'GET':		

        	return 'GET request received'

	elif request.method == "POST":			
		if 'msg' in request.args:
			return 'POST message received: ' + request.args['msg']
			
		
		return 'status code 200'
	

if __name__ == "__main__":
    	app.run(host="0.0.0.0", debug=True)
