FROM ubuntu:latest
LABEL authors="Avictor22"


# Set environment variables for silent installation
ENV MAYA_VERSION 2022
ENV MAYA_INSTALLER /tmp/maya/Autodesk_Maya_${MAYA_VERSION}_EN_Linux_64bit.tgz
ENV MAYA_INSTALL_DIR /usr/autodesk/maya${MAYA_VERSION}

# Copy the Maya installer to the container
COPY maya/ /tmp/maya

# Install required dependencies
RUN apt-get update && apt-get install -y \
    libssl1.0.0 \
    libtbb-dev \
    libpng-dev \
    libjpeg-dev \
    libx11-6 \
    libxcb1 \
    libgl1-mesa-glx \
    libgl1-mesa-dev \
    libglu1-mesa \
    libglu1-mesa-dev \
    libxrandr2 \
    libfreetype6 \
    libfreetype6-dev \
    libXcursor1 \
    libXi6 \
    libXinerama1 \
    libXcomposite1 \
    libasound2 \
    libdbus-glib-1-2 \
    libpangomm-1.4-1v5 \
    libpython2.7

# Extract and install Maya
RUN mkdir -p ${MAYA_INSTALL_DIR} && \
    tar -xzvf ${MAYA_INSTALLER} -C ${MAYA_INSTALL_DIR} --strip-components=1 && \
    rm -rf /tmp/maya

# Set the PATH and LD_LIBRARY_PATH environment variables
ENV PATH=${MAYA_INSTALL_DIR}/bin:$PATH
ENV LD_LIBRARY_PATH=${MAYA_INSTALL_DIR}/lib:$LD_LIBRARY_PATH

# Set the working directory
WORKDIR /app

# Set the entry point to launch Maya
ENTRYPOINT ["maya"]

# Define the default command to start Maya
CMD []
