
This program deals with sharing multiple lines of Anvi'o codes with a single YAML file.
If your data is already available online and you know the commands you need to run in order, this is the quickest way to reproduce it on another machine.

As you can see in the [anvi-run-batch tutorial](https://merenlab.org/), this program will run the commands in the setup and run section in the YAML file you provided sequentially.

## Running anvi-run-batch

A standard run of anvi-run-batch will look something like this:

{{ codestart }}
anvi-run-batch -y %(yaml)s \
               -o OUTPUT_DIR
{{ codestop }}

You should know that if you do not specify an output directory, your data will be downloaded to the home directory.

If you have made a change in the downloaded data and you want to delete it safely and download the same data again,
You can run the code below;

{{ codestart }}
anvi-run-batch -y %(yaml)s \
               -o OUTPUT_DIR/DATA_DIR \
               --reset --force-overwrite
{{ codestop }}

