# Random Forest vs Gradient Boosting: Ne Zaman Hangisini Seçersin?

İki ensemble modeli aynı veri seti üzerinde karşılaştırarak yalnızca metrik farklarını değil, modellerin veriye nasıl farklı baktığını gösteren bir analiz projesi. Aynı veri, farklı gözler: Random Forest yaşa odaklanırken Gradient Boosting ilişkisel duruma kilitleniyor.

## Veri Seti

**[Adult Income — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/2/adult)**

* 48.000+ satır, 13 özellik
* Hedef: Yıllık gelir >50K mı, ≤50K mı?
* Sınıf dağılımı: %75 ≤50K, %25 >50K (hafif dengesiz)

## Proje İçeriği

1. Veri yükleme ve temizleme (eksik değerler, kategorik kodlama)
2. Sınıf dağılımı analizi
3. Random Forest ve Gradient Boosting model eğitimi (100 ağaç, aynı koşullar)
4. Accuracy, Precision, Recall, F1 Score ve ROC-AUC hesaplama
5. Precision-Recall dengesi karşılaştırması
6. Feature importance analizi ve karşılaştırması
7. Eğitim süresi karşılaştırması
8. Metrik ve feature importance görsellerinin üretilmesi

## Sonuçlar

| Metrik | Random Forest | Gradient Boosting |
|--------|:---:|:---:|
| Accuracy | 0.8446 | 0.8620 |
| Precision | 0.7141 | 0.7917 |
| Recall | 0.6218 | 0.6017 |
| ROC-AUC | 0.8929 | 0.9179 |
| Eğitim Süresi | 1.04 sn | 5.84 sn |

**Feature Importance farkı:** RF → `age` (0.2131) · GB → `relationship` (0.3471) — aynı veri, tamamen farklı bakış açısı.

## Çalıştırma

Veri seti sklearn üzerinden otomatik indirilmektedir (`fetch_openml`).

```
pip install -r requirements.txt
python rf_vs_gb.py
```

## Kullanılan Teknolojiler

`Python` · `Pandas` · `Scikit-learn` · `Matplotlib` · `Seaborn` · `NumPy`

[![Medium](https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@zehranuracikgoz/random-forest-ve-gradient-boosting-neden-farkl%C4%B1-d%C3%BC%C5%9F%C3%BCn%C3%BCr-12fee0a48af3)
