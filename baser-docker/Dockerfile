FROM rocker/r-base

RUN R -e "install.packages(c('SuppDists'), repos='https://cran.rstudio.com/')"

# Add demo script
COPY demo.R demo.R
COPY R-benchmark-25.R R-benchmark-25.R

CMD ["R", "--no-save", "-f", "demo.R"]