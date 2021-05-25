# Using-Python-to-Interact-with-the-Operating-System-Working-with-Python-Scripts-

#!/usr/bin/env python3
import shutil
import psutil

def check_disk_usage(disk):
  du = shutil.disk_usage(disk)free = du.free / du.total *100
  return free >20
  
def check_cpu_usage():
  usage = psutil.cpu_percent(1)
  return usage <75
  
  
ifnotcheck_disk_usage("/") ornotcheck_cpu_usage():
  print("ERROR!")
else:
  print("Everything is OK!")
  
  
  
Requests is a Python module that you can use to send all kinds of HTTP requests. It's an easy-to-use library with a lot of features ranging from passing parameters in URLs to sending custom headers and SSL verification. You can add headers, form data, multi-part files, and parameters with simple Python dictionaries.You can then access the response data using the same request.

#!/usr/bin/env python3
import requests
import socket

def check_localhost():    
  localhost = socket.gethostbyname('localhost')
  return localhost =='127.0.0.1'

def check_connectivity():    
  request = requests.get("http://www.google.com")
  return request.status_code ==200
  
  
  
----IMPORT CONNECTIVITY MODULE

#!/usr/bin/env python3

from network import*
import shutil
import psutil

def check_disk_usage(disk):
"""Verifies that there's enough free space on disk"""    
  du = shutil.disk_usage(disk)    
  free = du.free / du.total *100return free >20

def check_cpu_usage():
  """Verifies that there's enough unused CPU"""    
  usage = psutil.cpu_percent(1)
  return usage <75
# If there's not enough disk, or not enough CPU, print an error

if notcheck_disk_usage('/') or not check_cpu_usage():
  print("ERROR!")
  
elifcheck_localhost() andcheck_connectivity():
  print("Everything ok")
  
else:print("Network checks failed")

