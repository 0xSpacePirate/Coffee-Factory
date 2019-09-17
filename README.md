# Coffee-Factory
For more information about the project see https://iwiki.eur.ad.sag/display/apama/Coffee+Factory+Blog



How to set up the project:


Designer: 

- Clone the repository


Prometheus:

- Go to https://prometheus.io/download/ and download Prometheus (should be on the very top) by choosing the file that corresponds to your OS.
- Install Prometheus to a suitable directory.
- Go to the folder which contains the installation and open the prometheus.yml file by right clicking on it and select a suitable text reader(notepad might not work), for example, I use Notepad++ to open it. Another thing you can do to open the file is: drag and drop the prometheus.yml file onto Designer.
- Once opened, at the very bottom make sure it looks like this:

  scrape_configs:
    # The job name is added as a label `job=<job_name>` to any timeseries scraped from this config.
    - job_name: 'prometheus'

    # metrics_path defaults to '/metrics'
    # scheme defaults to 'http'.

    static_configs:
    - targets: ['localhost:15903']

You will have to just set the 'targets' to ['localhost:15903'];

 
Grafana:

Firstly, follow this link: https://grafana.com/docs/guides/getting_started/
- Once you do the first two steps i.e. installation guide & logging in for the first time,
open the folder 'Grafana' in your Designer project and in it you would see a grafana.json file, copy the content of the file.
- Go to Grafana, click 'Create' (the plus button at the top left corner) and then click 'dashboard settings' (on top right) which will take you to another page.
- In that page click JSON model, paste here what you copied from the grafana.json file in Designer project.
- Click 'Save Changes'.



A photo of the project in action: https://imgur.com/a/2BEoMwF




