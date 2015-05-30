FROM aspirinsjl/genieacs

RUN curl -L https://get.rvm.io | bash -s stable 

RUN rvm install 2.0.0 && \
    rvm 2.0.0 --default

RUN gem install rails

RUN git clone https://github.com/zaidka/genieacs-gui.git /opt/git/genieacs-gui && \
    cd /opt/git/genieacs-gui/ && \
    cp config/graphs-sample.json.erb config/graphs.json.erb && \
    cp config/index_parameters-sample.yml config/index_parameters.yml && \
    cp config/summary_parameters-sample.yml config/summary_parameters.yml && \
    cp config/parameters_edit-sample.yml config/parameters_edit.yml && \
    cp config/parameter_renderers-sample.yml config/parameter_renderers.yml && \
    cp config/roles-sample.yml config/roles.yml && \
    cp config/users-sample.yml config/users.yml && \
    bundle
    
