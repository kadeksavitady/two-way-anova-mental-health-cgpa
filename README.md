# Two-Way ANOVA Analysis on Student Mental Health and CGPA

# Analisis Two-Way ANOVA pada Kesehatan Mental dan IPK Mahasiswa

>>>

## !!! Warning / Peringatan

Meskipun proyek ini membahas topik kesehatan mental, dataset yang digunakan
**tidak mengandung data pribadi atau identitas individu**.

Proyek ini menggunakan **data sekunder yang bersifat publik** dan ditujukan **hanya untuk kepentingan akademik dan pembelajaran**. Hasil analisis **tidak dimaksudkan sebagai kesimpulan medis atau klinis**.

>>>

## Overview (English)

This project analyzes the effect of mental health factors on students’ academic performance (CGPA) using the Two-Way ANOVA method. The main goal is to see whether **Gender** and **Anxiety**, as well as their interaction, have a significant effect on CGPA.

The dataset used is the *Student Mental Health* dataset from Kaggle. The analysis is done using Python and basic statistical methods that are commonly taught in early data science courses.

>>>

## Gambaran Umum (Bahasa Indonesia)

Proyek ini menganalisis pengaruh faktor kesehatan mental terhadap IPK (CGPA) mahasiswa menggunakan metode **Two-Way ANOVA**. Fokus utama adalah melihat apakah **Gender** dan **Anxiety**, serta interaksi di antara keduanya, berpengaruh terhadap IPK mahasiswa.

Dataset yang digunakan berasal dari Kaggle dengan judul *Student Mental Health*. Analisis dilakukan menggunakan Python dan metode statistik dasar yang masih relevan untuk mahasiswa semester awal.

>>>

## Dataset

**English**

* Data Source: Kaggle – *Student Mental Health Dataset*
[https://www.kaggle.com/datasets/shariful07/student-mental-health]
* Total observations: 100 records
* Target variable (Dependent):

  * `CGPA` (converted from range into numeric midpoint)
* Independent variables:

  * `Gender` (Female / Male)
  * `Anxiety` (Yes / No)
* Data collected from a survey of IIUM students using Google Forms.

**Bahasa Indonesia**

* Sumber Data: Kaggle – *Student Mental Health Dataset*
[https://www.kaggle.com/datasets/shariful07/student-mental-health]
* Jumlah data: 100 mahasiswa
* Variabel target (dependen):

  * `CGPA` / IPK (diubah dari rentang menjadi nilai tengah numerik)
* Variabel independen:

  * `Gender` (Perempuan / Laki-laki)
  * `Anxiety` (Ya / Tidak)
* Data dikumpulkan melalui survei mahasiswa IIUM menggunakan Google Form.

>>>

## Methodology | Metodologi

1. **Data Preprocessing / Pra-pemrosesan Data**
   * Membersihkan spasi berlebih pada kolom
   * Mapping data kategori menjadi numerik:

     * Gender → 0 (Female), 1 (Male)
     * Anxiety → 0 (No), 1 (Yes)
   * Mengubah CGPA dari rentang menjadi nilai tengah
   * Menghapus missing value
   * Memastikan CGPA bertipe numerik

2. **Exploratory Data Analysis (EDA)**
   * Statistik deskriptif tiap kelompok
   * One-Way ANOVA awal untuk melihat variabel yang paling mendekati signifikan

3. **Assumption Checking / Uji Asumsi**
   * Normalitas residual → Shapiro-Wilk Test
   * Homogenitas varians → Levene’s Test

4. **Data Transformation (Optional)**
   * Transformasi sqrt dan log pada CGPA
   * Bertujuan memperbaiki distribusi data

5. **Modeling / Pemodelan**
   * Two-Way ANOVA
   * Model:

     ```
     CGPA ~ Gender + Anxiety + Gender*Anxiety
     ```

6. **Post Hoc Test**
   * Tukey HSD
   * Digunakan untuk melihat perbedaan antar kelompok jika ada indikasi signifikan

>>>

## Results | Hasil Analisis

**English**

* Gender, Anxiety, and their interaction do not show significant effects on CGPA (p-value > 0.05).
* Gender has the closest p-value to significance (≈ 0.075), showing a small indication but not strong enough statistically.
* Data transformation (sqrt and log) improves distribution but does not change the final conclusion.
* The model explains only a small part of CGPA variation (R² ≈ 6%).

**Bahasa Indonesia**

* Gender, Anxiety, dan interaksinya tidak berpengaruh signifikan terhadap CGPA (p-value > 0.05).
* Variabel Gender paling mendekati signifikan (p ≈ 0.075), tetapi masih belum cukup kuat secara statistik.
* Transformasi data membantu memperbaiki distribusi, namun tidak mengubah hasil utama.
* Model hanya mampu menjelaskan sebagian kecil variasi CGPA (R² ≈ 6%).

>>>

## Key Takeaways | Kesimpulan Utama

* Two-Way ANOVA digunakan untuk melihat pengaruh dua variabel kategori terhadap satu variabel numerik.
* Dalam dataset ini, **Gender dan Anxiety tidak terbukti berpengaruh signifikan terhadap IPK**.
* Transformasi data penting untuk membantu asumsi, tetapi tidak selalu mengubah hasil analisis.
* Ukuran data yang kecil dan distribusi responden yang tidak seimbang dapat memengaruhi hasil.
* Walaupun tidak signifikan, ada pola kecil yang bisa jadi bahan penelitian lanjutan.

>>>

## Tools & Libraries

* Python
* Pandas, NumPy
* Scipy
* Statsmodels
* Matplotlib, Seaborn

>>>

## Author

Kadek Savita Dyutianaya
Applied Data Science Student

Politeknik Elektronika Negeri Surabaya

