FROM ipython/scipyserver

########################################
#
# Image based on ipython/scipyserver
#
#
# docker run -d -p 444:8888 -e "PASSWORD=ASD" --volumes-from scipy-data l0rth0s/scipyserver
#######################################

# Install opencv prerequisites...
RUN apt-get update -qq && apt-get install -y --force-yes \
            libopencv-dev \
            python-opencv;

# Additional python modules
RUN pip2 install imutils
RUN pip3 install imutils

VOLUME /notebooks
WORKDIR /notebooks