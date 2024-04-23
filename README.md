# Workload-Aware SQL Query Recommendation Using Deep Learning

This file has got all the errors that we encountered while analysing, fixing and running the files. Treat this as a FAQ file for your research on this project.

**FAQ's**

1. Python Versions: 3.9 or 3.11. Some of the errors occur due to the libraries that 3.9 version had, so install the 3.9 verison of     Python when you encounter errors in 3.11.

2. Import.py is unresponsive so try importing all the necessary functions in each coding file. Technically, hardcode the necessary import fucntions in each file. Before importing install the packages that are missing by using "pip install followed by the package name". Check your versions using "pip list".

3. scripts/data_processing/model_data/process_sequences.py
    Use pull_human_sessions.sql to get humansession.csv
    Replace ID and numeric values with <ID> and <NUM> respectively. Now we will get humansession_parsed.csv

4. scripts/data_processing/model_data/process_templates.py
   Replace the DIR_PATH with the path to qdict_statements.csv on your computer.
   Make sure sdss_tree_template.csv  is also in the same path.

5. scripts/models/dataloader.py
   Change the data_dir to a path on your computer (264)
   Datafile path should be to train.txt file in sdss/model_data/classification/train.txt

6. scripts/models/eval.py
   csvfile ———>cvfile (391)
   calc_recall—————>recall( 392)
   calc_precision————->precision (393)
   trgs———> tag (392,393)
   Preds———->pred (392,393)
   Wrong declaration of variables. Hence change them the way its listed above. The numbers in the brackets the line numbers but this may    vary so just look for the variables and then make the changes. 

7. scripts/models/seq_generator.py
   Change data_dir path
   Change model path to location of transformer_pred_sdss.pth on your computer.

8. scripts/models/template.py
   q_src ——> src(113)

9. scripts/models/utils.py
   EOS_TOKEN ——>EOS_token (53, 55)
   SOS_TOKEN——->SOS_token (54)

10. scripts/pipelines/class_eval.py
    Load setup_final file from wandb directory
    Change the setup_config path(24)
    Remove global variables in lines 268 and 273

11. scripts/pipelines/eval_test.py
    Change the data_dir and model_pth to the path to cnn_pred_sdss.pth


12. scripts/pipelines/fine_tuning.py
    Change wandb_dir to path in your computer
    Load setup.yaml file from wandb directory
    Change the setup_config path
    Remove global variables in lines 232 and 237

13. scripts/pipelines/model_eval.py
    Change wandb_dir to path in your computer
    Remove global variables in lines 151, 155 and 160

14. scripts/pipelines/seq2seq_training.py
    Change setup_config path(17)
    Change wandb_dir to path in your computer
    Remove global variables (136, 140 and 145)

15. If you get an path error then thats beacuse of the missing file "setup_final". This can be fixed by contacting the author of the project either via LinkedIn or mailing her.
16. We are including the links to the thesis paper and the original source code of this project for your reference.
    https://github.com/ey-l/Workload-Aware-SQL-Query-Recommendation-Using-Deep-Learning/tree/main
    https://openproceedings.org/2023/conf/edbt/paper-173.pdf

