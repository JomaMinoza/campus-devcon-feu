FROM jupyter/scipy-notebook

ENV OPENAI_API_KEY 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

RUN conda install --quiet --yes \
    'mlflow' \
    'psycopg2' \
    'keras' \
    'xgboost' \
    'python-graphviz' \
    'imbalanced-learn' \
    'google-cloud-storage' \
    'nb_conda' \
    'jupyter_contrib_nbextensions' \
    'jupyter_nbextensions_configurator' 

RUN pip install --user --upgrade \
    'scikit-learn' \
    'google-cloud' \
    'google-cloud-bigquery' \
    'google-cloud-storage'

RUN pip install --user \
        'handcalcs' \
        'pmdarima' \
        'geopy' \
        'chord' \
        'jupyter_http_over_ws' \
        'openai' \
        'openai-whisper' \
        'huggingface_hub' \
        'transformers'


RUN jupyter contrib nbextension install --user 
RUN jupyter nbextensions_configurator enable --user
RUN jupyter nbextension enable jupyter_http_over_ws --sys-prefix

USER root

USER $NB_UID