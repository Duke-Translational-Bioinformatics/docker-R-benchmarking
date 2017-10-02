FROM nuest/docker-mro

#RUN R -e "install.packages(c('SuppDists'), repos='https://cran.r-project.org/')"

# Add demo script
COPY demo.R demo.R
COPY R-benchmark-25.R R-benchmark-25.R

CMD ["R", "--no-save", "-f", "demo.R"]