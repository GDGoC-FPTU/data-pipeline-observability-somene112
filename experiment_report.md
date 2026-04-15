# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600150  
**Name:** Nguyen Duc Hoang Phuc  
**Date:** 15/04/2026  

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200. | 10 | Du lieu da duoc validate, khong co gia tri loi |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999. | 3 | Bi anh huong boi outlier va du lieu khong hop le |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi su dung garbage data, Agent tra loi sai do du lieu dau vao khong dam bao chat luong. Cu the, bo du lieu chua nhieu van de nhu duplicate ID (ID bi trung), wrong data type (gia la string "ten dollars"), null values (category va id bi thieu), va outlier (gia qua lon nhu 999999). Agent simulation hien tai chi dua tren logic don gian (chon san pham co gia cao nhat trong category), nen khong co co che phat hien du lieu bat thuong.

Do do, record "Nuclear Reactor" voi gia tri cuc lon duoc chon lam "best choice", mac du day la du lieu khong thuc te. Dieu nay cho thay Agent khong tu hieu duoc chat luong du lieu, ma chi xu ly theo logic da duoc lap trinh. Neu khong co buoc validation manh, cac loi du lieu se truc tiep dan den ket qua sai lech.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** → Dong y.

Chat luong du lieu dau vao co anh huong quyet dinh den ket qua cua Agent. Du prompt co tot den dau, neu du lieu dau vao bi loi hoac nhiem ban (poisoned), Agent van dua ra ket qua sai. Thi nghiem nay cho thay viec dam bao data quality (thong qua validation, cleaning, anomaly detection) quan trong hon viec chi cai thien prompt.