FROM continuumio/miniconda3

RUN conda update conda \
  && conda update --all \
  && conda install jupyter numpy pandas matplotlib \
  && conda clean --all

RUN pip install -U pip \
  && pip install pandas-profiling pixiedust