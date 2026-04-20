# Self-Pruning Neural Network Results

## 📊 Training Summary

### Lambda = 1e-05
| Epoch | Loss     |
|------|----------|
| 1    | 3755.62  |
| 2    | 3197.99  |
| 3    | 2766.32  |
| 4    | 2420.36  |
| 5    | 2143.95  |

- **Test Accuracy:** 55.03%  
- **Sparsity Level:** 0.04%

---

### Lambda = 1e-04
| Epoch | Loss     |
|------|----------|
| 1    | 31346.99 |
| 2    | 26061.26 |
| 3    | 21259.88 |
| 4    | 17112.77 |
| 5    | 13709.13 |

- **Test Accuracy:** 54.39%  
- **Sparsity Level:** 0.08%

---

### Lambda = 1e-03
| Epoch | Loss      |
|------|-----------|
| 1    | 307419.59 |
| 2    | 255074.88 |
| 3    | 206852.25 |
| 4    | 164814.58 |
| 5    | 130032.93 |

- **Test Accuracy:** 53.20%  
- **Sparsity Level:** 0.08%

---

## 📈 Final Comparison Table

| Lambda | Test Accuracy (%) | Sparsity (%) |
|--------|------------------|-------------|
| 1e-05  | 55.03            | 0.04        |
| 1e-04  | 54.39            | 0.08        |
| 1e-03  | 53.20            | 0.08        |

---

## 🔍 Observations

- Increasing λ increases sparsity slightly, but not significantly in this setup.
- Accuracy decreases as λ increases, showing the trade-off between pruning and performance.
- Sparsity remains very low, suggesting:
  - λ values may still be too small  
  - More training epochs may be needed  
  - Stronger regularization or temperature scaling could help  

---

## ⚠️ Key Insight

The model is **learning slowly to prune**, but current sparsity levels (<0.1%) indicate that:
- Gates are not collapsing to zero aggressively
- Further tuning is required for effective self-pruning

---
