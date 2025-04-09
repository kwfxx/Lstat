import os
import requests
from user_agent import generate_user_agent
from time import time
from hashlib import md5
from random import choice
from concurrent.futures import ThreadPoolExecutor
from cfonts import render, say
from requests import post as pp
from user_agent import generate_user_agent as gg
from random import choice as cc
from random import randrange as rr
import random
import base64
import re
import ethan
import sys
from asmix import Instagram
import random
import string
import json
import requests
from threading import Thread
from rich.console import Console
Con = Console()
Ex = 0
def Users():
    global Ex
    try:
        
        LsD = ''.join(random.choices(string.ascii_letters + string.digits, k=4))
       
        UseriD = str(random.randrange(900000,uid))
        
        variables = json.dumps({"id": UseriD, "render_surface": "PROFILE"})
        data = {"lsd": LsD, "variables": variables, "doc_id": "25618261841150840"}
        
        response = requests.post("https://www.instagram.com/api/graphql", headers={"X-FB-LSD": LsD}, data=data)
        
        
        username = response.json()['data']['user']['username']
        with open('username.txt', 'a') as f8:
        	f8.write(f'{username}\n')
        Ex += 1
        Con.print(f"[{Ex}] Username : [green]{username}")
        
    
        return username
    except Exception as e:
    	return None

print('''
1 -  2011
2 - 2012
3 - 2013
4 - 2014
5 - 2015
6 - 2016-2017
''')
num = int(input('choice<=> : '))


if num == 1:
    uid = 18957417
    iud = 10000
elif num == 2:
    uid = 287924624
    iud = 18314009
elif num == 3:
    uid = 461365132
    iud = 180165130
elif num == 4:
    iud = 361365132
    uid = 1682665388
elif num == 5:
    iud = 1682665388
    uid = 3382665388
elif num == 6:
    iud = 2682665388
    uid = 8682665388
else:
    exit()
def ExUsers():
    for _ in range(1000):  
        Users()

threads = []
for _ in range(100): 
    thread = Thread(target=ExUsers)
    thread.start()
    threads.append(thread)

for thread in threads:
    thread.join()

Con.print(f"</> Users Extracted: [bold]{Ex}[/bold]")
