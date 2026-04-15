(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)

[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574086&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** ndhphuc2005@gmail.com 
**Name:** Nguyen Duc Hoang Phuc

---

## Mo ta

Bai lab nay xay dung mot ETL pipeline gom 4 buoc: Extract, Validate, Transform va Load.  
Toi da doc du lieu tu file JSON, loai bo cac record khong hop le (gia <= 0, category rong), sau do transform du lieu bang cach tinh gia sau giam 10% va chuan hoa category. Cuoi cung, du lieu duoc luu ra file CSV.  

Ngoai ra, toi thuc hien mot thi nghiem so sanh giua clean data va garbage data de danh gia anh huong cua data quality den ket qua cua AI Agent.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python generate_garbage.py
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Pipeline da xu ly thanh cong du lieu:

- Tong so record ban dau: 5
- So record hop le: 3
- So record bi loai: 2

Cac record bi loai do gia <= 0 hoac category rong. Ket qua cho thay ETL pipeline hoat dong dung, tuy nhien garbage data van co the gay anh huong den ket qua cua Agent neu khong co validation nang cao.