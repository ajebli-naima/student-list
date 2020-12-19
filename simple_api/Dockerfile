FROM python:2.7-stretch
#Maintainer of image
LABEL maintainer="naiimaajebli@gmail.com"
#Install of dependencies
RUN apt-get update && apt-get install python-dev python3-dev libsasl2-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python_dotenv
#Add source code in the image
ADD student_age.py /
#Create Data Folder
VOLUME [ "/data" ]
#Export  port
EXPOSE 5000
#Run code
ENTRYPOINT ["python"]
CMD ["./student_age.py"]


