#Create docker image with dockerfile"

#download based image from dockerfile.com

FROM python:3.12-slim

#create new app folder in linux image

WORKDIR /app
#ek folder app ka nam bn jaega

#COPY from based-operating system to linux image
#Copy source distribution
#copy everything from source operating system to target operating stem (linux image)

COPY . ./app 

#1st dot means all/everything, to jb m command chlaungha dockerfile k barabar sy to waha jytni cheezen hen, dockerfile,image,folders 
#to ap ne jtni b files bnai hongi wo sari app k folder m copy pastebhojaengi
#2nd dot means root folder m utha kr rakh dy
#download based image from dockerfile.com


#jb b m is code ko chlaun to image k andar ek or command likni hoti hy cmd k zarye

#RUN PYTHON FILE CODE
#LOCAL COMP SY UTH KT LINUX M CHALI GAE 
#JAHA PR DOCKERFILE MOJUD HY WAHA APKI CMD HONI CHAHYE

CMD python./app/my_code.py

#Create image with docker file
'docker build -t<my-dev-image> . ' <br>
#br yani html crack b markdown support krta hy
optional command
if u want to create image with any specific env like dev,test,opt then use below command

'docker build -f Dockerfile.dev -t <my-dev-image>.'

docker build -t ned .
