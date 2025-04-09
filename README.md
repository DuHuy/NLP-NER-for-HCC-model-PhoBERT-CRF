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

                 precision    recall  f1-score   support

        CQ       0.89      0.92      0.91     19516
          NG       0.97      1.00      0.99       481
          SL       0.97      1.00      0.98       496
        VBPL       1.00      1.00      1.00        44
          ĐT       0.60      0.69      0.64      4925

   micro avg       0.83      0.88      0.86     25462
   macro avg       0.89      0.92      0.90     25462
weighted avg       0.84      0.88      0.86     25462

True label counts: Counter({'O': 1148544, 'I-SL': 63488, 'I-NG': 61568, 'B-CQ': 19456, 'I-ĐT': 7808, 'I-CQ': 7680, 'I-VBPL': 5632, 'B-ĐT': 4864})
Predicted label counts: Counter({'O': 1141100, 'I-SL': 63578, 'I-NG': 63232, 'B-CQ': 20095, 'I-ĐT': 11527, 'I-CQ': 8372, 'I-VBPL': 5632, 'B-ĐT': 5504})
