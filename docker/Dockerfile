FROM python:2
ENV NB_USER hzm5196
ENV NB_UID 25678
ENV CONDA_DIR /opt/conda

RUN useradd -m -s /bin/bash -N -u $NB_UID $NB_USER && \
    mkdir -p $CONDA_DIR && \
    chown $NB_USER $CONDA_DIR -R && \
    mkdir -p /src && \
    chown $NB_USER /src

USER hzm5196
RUN conda install --name python
RUN pip install scipy matplotlib intervaltree bokeh magenta requests tensorflow
EXPOSE 8888
ENV LD_LIBRARY_PATH /usr/local/nvidia/lib64:$LD_LIBRARY_PATH
