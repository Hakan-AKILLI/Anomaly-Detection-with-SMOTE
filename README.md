# 🛡️ Network Intrusion Detection with SMOTE & Random Forest

Bu proje, ağ trafiği üzerindeki siber saldırıları (DoS, Probe, U2R, R2L) tespit etmek amacıyla geliştirilmiş çok katmanlı bir Makine Öğrenmesi (Yapay Zeka) Güvenlik Duvarı simülasyonudur.

## 🎯 Projenin Amacı ve Çözülen Problem
Siber güvenlik veri setlerinde (KDDTrain+) en büyük problem **Sınıf Dengesizliğidir (Class Imbalance)**. Normal trafik ve DoS saldırıları on binlerce satır iken, sisteme tam yetkiyle sızmaya çalışan en tehlikeli saldırılar (U2R - Root yetkisi) sadece birkaç satırdır.

Standart makine öğrenmesi algoritmaları (örn: Baseline Decision Tree) bu dengesizlikte azınlık sınıflarını ezberler ve gerçek dünyada çuvallar. Bu projede:
1. **SMOTE (Synthetic Minority Over-sampling Technique)** kullanılarak azınlık sızma saldırıları sentetik olarak çoğaltılmış ve veri dengelenmiştir.
2. Artan karmaşıklığı yönetmek ve Overfitting'i önlemek için tek bir Karar Ağacı yerine **Random Forest (100 Ağaçlık Rastgele Orman)** mimarisi kurulmuştur.

## 🚀 Elde Edilen Başarılar (Sonuçlar)
- Dışarıdan sisteme sızma girişimlerini içeren **R2L (Sızma) saldırılarında %99 Yakalama Oranı (Recall)** ve %100 Nokta Atışı (Precision) elde edilmiştir.
- Baseline modelin ezberleyerek yanıldığı U2R (Root) saldırılarında, False Positive (Yanlış Alarm) oranı minimize edilerek Precision değeri %58'den **%86'ya** çıkarılmıştır.
- Modelin kararları **Feature Importance** ve **Confusion Matrix** ısı haritalarıyla analiz edilerek şeffaflaştırılmıştır.

## 🛠️ Kullanılan Teknolojiler
- **Dil:** Python
- **Veri Manipülasyonu & Analiz:** Pandas, NumPy, Matplotlib, Seaborn
- **Makine Öğrenmesi:** Scikit-Learn (Random Forest, Decision Tree)
- **Veri Dengeleme:** Imbalanced-Learn (SMOTE)
