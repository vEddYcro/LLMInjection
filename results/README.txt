MFLP run 20260912T161140Z_llama3.3_70b-instruct-q4_K_M
model: llama3.3:70b-instruct-q4_K_M
pilot: 0
robustness: 0   (1 = second-model replication corpus, NOT for investigators)

investigator_I1.zip .. investigator_I5.zip
    Hand exactly one of these to each investigator. They contain blinded evidence
    packages, a pre-populated workbook.csv, and the instructions. Nothing else.

study_team_PRIVATE_DO_NOT_SHARE.zip
    Canonical L4 traces, sealed ground truth, the opaque-token map, and the run
    manifest. Investigators must not receive this before responses are locked.

analysis_outputs.zip
    Design, power, cost tables and figures 1-8.

After collecting completed workbooks into collected/I1/workbook.csv .. collected/I5/workbook.csv:
    python3 score_study.py --responses collected/ --out deliverables/results
