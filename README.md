# RNAdegformer-WebApp

I made this web application (inspired by https://github.com/fatihozturkh2o/explorna_wave
) using h2o's wave so that RNAdegformer models can be used easily. In addition, if your computer is too slow to run the app, you can also use Kaggle notebooks (you get 40 free GPU hours per week) I created to use the models:


https://www.kaggle.com/shujun717/nucleic-transformer-rna-degradation-inference <br />

## Showcase

### Home page
![home_page](https://github.com/Shujun-He/RNAdegformer-Webapp/blob/main/files/home_page.png)



### RNA degradation prediction
In this page you can predict RNA degradation at each nucleotide and visualize the attention weights of the Nucleic Transformer

![RNA degradation](https://github.com/Shujun-He/RNAdegformer-Webapp/blob/main/files/rnapage.png)



## How to run
Clone the repo to your local linux machine (I recommend Ubuntu). Then create an environment:
```bash
conda create -n RNA python==3.8
conda activate RNA
```

Before everything make sure that wave is ready. Use this version of wave: https://github.com/h2oai/wave/releases/tag/v0.10.0

To install and and start the wave server:
```bash
wget https://github.com/h2oai/wave/releases/download/v0.10.0/wave-0.10.0-linux-amd64.tar.gz
tar -xvzf wave-0.10.0-linux-amd64.tar.gz
cd wave-0.10.0-linux-amd64
./waved &
```

This needs to be running for the app to work. So leave the terminal with waved running and open a new one to do the rest of the setup

**1.** Open terminal in the cloned folder and run: <code>make setup</code>

**2.** Then run the bash file: for Ubuntu: <code>bash Ubuntu_setup_draw_rna.sh</code> , for Mac: <code>bash MacOS_setup_draw_rna.sh</code>

**3.** Now you are ready to run the app: <code>./venv/bin/python run.py</code>   

**3.** Go to <code>http://localhost:10101/rnadegformer</code> in your browser.
