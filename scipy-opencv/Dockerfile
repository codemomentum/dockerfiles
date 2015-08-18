FROM ipython/scipyserver

########################################
#
# Image based on ipython/scipyserver
#
#   added OpenCV 3 (built)
#   plus prerequisites...
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