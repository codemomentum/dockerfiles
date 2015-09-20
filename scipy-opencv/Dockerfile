FROM ipython/scipyserver

RUN pip install --upgrade pip

########################################
#
# Image based on ipython/scipyserver
#
#
# docker run -d -p 444:8888 -e "PASSWORD=XXX" --volumes-from scipy-data l0rth0s/scipyserver
# docker run -d -p 444:8888 -e "PASSWORD=XXX" -v /root/notebooks:/notebooks l0rth0s/scipyserver
#######################################

# Install opencv prerequisites...
RUN apt-get update -qq && apt-get install -y --force-yes \
            libopencv-dev \
            python-opencv;


# Additional python modules
RUN pip2 install imutils
RUN pip3 install imutils

#RUN pip2 install bokeh
#RUN pip3 install bokeh

RUN pip2 install ggplot
RUN pip3 install ggplot

RUN pip2 install mpld3
RUN pip3 install mpld3

RUN pip2 install vincent
RUN pip3 install vincent

RUN pip2 install keras
RUN pip3 install keras


RUN pip2 install textblob
RUN pip3 install textblob
RUN python -m textblob.download_corpora





VOLUME /notebooks
WORKDIR /notebooks
