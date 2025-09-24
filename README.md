
# 🎬 Movie Dataset Analysis

## 📌 Overview
This project analyzes a large-scale movie dataset (`movies.csv`) sourced from **Kaggle**, containing **999,999 records** and **17 columns**.  


The goal is to uncover **financial, cultural, and temporal patterns** in the film industry through exploratory data analysis (EDA) and visualization.  

## 📊 Dataset
**Shape**: `(999,999, 17)`  
**Key Columns**:
- `Title`, `Genre`, `ReleaseYear`, `ReleaseDate`, `Country`
- `BudgetUSD`, `US_BoxOfficeUSD`, `Global_BoxOfficeUSD`
- `Opening_Day_SalesUSD`, `One_Week_SalesUSD`
- `IMDbRating`, `RottenTomatoesScore`, `NumVotesIMDb`, `NumVotesRT`
- `Director`, `LeadActor`

## 🔍 Key Insights
1. **Top 10 Movies by ROI and Rating**  

   - Identified the most profitable movies relative to budget and critical reception. 
   - **Seek bed** was the top movie by IMDbRating (10.0) anf ROI values (6.0)

 <br>

2. **Box Office vs IMDb Rating**  

   - Scatter plot with a weak **negative correlation (r = -0.05)** → suggesting there is little to no linear relationship. This indicates that critical reception (IMDb scores) does not strongly predict commercial success.

<br>

3. **Average Box Office by IMDb Rating** 

   - Showed general trends of earnings across different rating levels.  

 <br>

4. **Number of Movies Released per Year**  

   - Consistent growth over time: from **2,432 movies (in 1950)** to **23,809 movies (in 2025)**.  

 <br>

5. **Average Box Office by Release Month** 

   - **July, September, and December** emerged as peak months for box office earnings, reflecting **holiday and blockbuster seasons**. 

<br>

   ![Alt text](<photos/box office month.png>)

6. **Genres: Artistic vs Financial Success**  

   - Genre-level analysis revealed **Documentary, Horror, and Thriller** as financially successful genres.  

<br>

   ![Alt text](<photos/Genres scatter.png>)

7. **Top Countries by Avg Global Box Office**  

   - **UK** ranked highest in average global earnings.  

<br>

8. **Momentum Analysis (Opening vs First Week)**  
   - Introduced a *Momentum Ratio* = `One_Week_Sales / Opening_Day_Sales`.  
   - Movies with high ratios showed strong word-of-mouth growth.  
 <br>

   ```
   movies['Momentum'] = movies['One_Week_SalesUSD'] /movies['Opening_Day_SalesUSD']
   top_momentum = movies[['Title','Momentum']].sort_values(by='Momentum', 
   ascending=False).head(10)
   ```
   - **"Reduce Rule"** ranked as the top momentum-driven film.  
 <br>

9. **Top 5 Directors by Avg Global Box Office**  
   - **Albert Philips** led the ranking.  
<br>

10. **Top 5 Lead Actors by Avg Global Box Office**  
    - **Eric Obrien** topped the list.  
<br>

    ![Alt text](<photos/talent.png>)


## 🛠️ Tools & Libraries
- **Python**  
- **Pandas** (data manipulation)  
- **Matplotlib / Seaborn** (visualization)  
- **NumPy** (mathematical operations)  

## 📈 Future Work
- Build predictive models to estimate box office success based on budget, rating, and genre.  
- Compare US vs Global revenue patterns for regional insights.  
- Deeper analysis of directors and actors across decades.  

## 📂 Source
Dataset: [Kaggle Movies Dataset](https://www.kaggle.com/datasets/mjshubham21/movie-dataset-for-analytics-and-visualization)  

---

