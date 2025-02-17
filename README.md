# Ner-for-hcc-vietnamese
### Số lượng nhãn trong tập train:
##### O: 2260705
##### CQ: 68637
##### VBPL: 74484
##### ĐT: 88407
##### NG: 55929
##### SL: 45954

### Số lượng nhãn trong tập test:
##### O: 199407
##### ĐT: 13140
##### NG: 8174
##### CQ: 9507
##### VBPL: 3854
##### SL: 1517

#### Số lượng mẫu trong tập train: 111358
#### Số lượng mẫu trong tập test: 10000
### Phobert
    dropout=0,3,
    learning_rate=3e-5,
    save_steps=300,  # Lưu checkpoint mỗi 500 bước
    logging_steps=50,  # Hiển thị log sau mỗi 50 bước
    per_device_train_batch_size=16,
    per_device_eval_batch_size=16,
    num_train_epochs=4,  # Số epoch
    weight_decay=0.01,
.
              precision    recall  f1-score   support

        B-CQ       1.00      1.00      1.00      7105
        B-NG       1.00      1.00      1.00      4087
        B-ĐT       1.00      0.99      0.99      7109
        I-CQ       0.96      1.00      0.98      2402
        I-NG       1.00      1.00      1.00      4087
        I-ĐT       0.99      0.97      0.98      6031
           O       1.00      1.00      1.00    199407

    accuracy                           1.00    230228
   macro avg       0.99      0.99      0.99    230228
weighted avg       1.00      1.00      1.00    230228
