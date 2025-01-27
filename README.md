![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-ffb6c1?style=for-the-badge&logo=seaborn&logoColor=white)

# EDA-Volleybal-National-League-

This project performs Exploratory Data Analysis (EDA) on Volleyball National League (VNL) data. The analysis aims to uncover patterns and insights related to player performance, team contributions, and game trends across different metrics such as attack, block, serve, and dig.

### Goals of the Analysis
To analyze and visualize the performance metrics of players in the Volleyball National League (e.g., attack, block, serve, etc.).
To identify top-performing players and countries based on specific metrics like the highest attack and block values.
To explore age-wise and position-wise trends in player performance.
To provide insights into team-level contributions and their impact on the league

### About Dataset
 Hello everyone!

I've started collecting and sorting a dataset about volleyball players in the Volleyball National League in 2023.

The recourse I've used is volleyballworld.com

In each factor, I used the average of the player during a game, which was the author of errors, points, and percentage of positive performance of that player in each section.

Here are some information about the Dataset:

Position Feature represents the real position of each player.r

**OH**: outside hitter

**OP**: Opposite hitter

**M**: Middle blocker

**S**: Setter

**L**: Libero

**Attack**:  A player's overall average during each game in the offense factor

**Block**: A player's overall average during each game in the defense factor.

**Defense**: on the net includes direct points, errors, and touching the ball without changing points.

**Serve**: Except for the libero player, the rest of the players serve during each turn to start the game. Each player's service average during the match is listed here.

**Set **: The setter is responsible for setting the players. But in special cases, the rest of the players cooperate in this matter, and in the data analysis, we will find out which position the players have the most participation in setting after the setter.

The set feature represents the average of successful sets, errors, and attempts for each ball during a rally.
**Dig**: the average of digs, errors, and reception.ns

**Receive**: Receive feature also represents the average of successful receptions, errors r, rs, and attempts per match.


Here is the basic diagram of players on the court


![vnl](https://github.com/user-attachments/assets/2b667a5c-dc49-43ff-8945-f38e6c2a669d)


### GitHub README - Volleyball National League Analysis  

---

####  **Getting Started**  

**Prerequisites**  
- **Python 3.6+**: Download from [python.org](https://www.python.org/downloads/).  
- **Jupyter Notebook**: Installed via `pip` (see below).  

---

#### 🔧 **Installation**  
1. **Clone the Repository**:  
   ```bash  
   github.com/kkr007007/EDA-Volleybal-National-League-   
   ```  

2. **Install Required Libraries**:  
   ```bash  
   pip install pandas numpy matplotlib seaborn jupyter  
   ```  

3. **Download Data & Assets**:  
   - **Dataset**: Download `VNL2023.csv` and place it in the project folder.  
   - **Image**: Download `vnl.jpg` (used in the pie chart visualization) and save it to the project folder.  

---

####  **Running the Jupyter Notebook**  
1. **Launch Jupyter Notebook**:  
   ```bash  
   jupyter notebook  
   ```  
   This will open Jupyter in your browser.  

2. **Open the Notebook**:  
   - Navigate to `Volleyball_National_League_Analysis.ipynb` and open it.  

3. **Execute Cells**:  
   - Run each cell sequentially using **Shift + Enter**.  
   - Ensure the notebook has access to `VNL2023.csv` and `vnl.jpg` (place them in the same directory).  



Now you’re ready to dive into the analysis! 🏐✨



### Key Insights


#### **1. Data Overview**  
- **Total Players**: 131 players from **16 countries** (Japan, Italy, France, Cuba, Bulgaria, etc.).  
- **Positions**:  
  - **OH** (Outside Hitter): 42 players (32.1%)  
  - **MB** (Middle Blocker): 32 players (24.4%)  
  - **OP** (Opposite): 25 players (19.1%)  
  - **L** (Libero): 16 players (12.2%)  
  - **S** (Setter): 16 players (12.2%)  
- **Data Quality**: No missing values (`a.isna().sum() = 0`).  

---

#### **2. Player Demographics**  
- **Age Distribution**:  
  - **Mean**: 27.8 years (±4.2 years).  
  - **Oldest Player**: 41 years (Teodor Salparov, Libero from Bulgaria).  
  - **Youngest Player**: 19 years (Leonard Graven, Libero from Germany).  
  - **Peak Age Group**: 25–30 years (40% of players).  

---

#### **3. Skill Performance Highlights**  
| Skill       | Mean   | Max Value | Top Performer (Country, Position)       |  
|-------------|--------|-----------|------------------------------------------|  
| **Attack**  | 5.64   | 15.80     | Ichikawa Yuki (Japan, OH)                |  
| **Block**   | 0.85   | 4.08      | Unnamed MB player (likely highest block) |  
| **Serve**   | 0.54   | 2.08      | Nimir Abdel-Aziz (Nederland, OP)         |  
| **Dig**     | 3.43   | 11.44     | Unnamed Libero (likely highest dig)      |  
| **Receive** | 1.68   | 6.69      | Unnamed Libero (likely highest receive)  |  
| **Set**     | 2.19   | 26.89     | Unnamed Setter (likely highest set)      |  

---

#### **4. Correlations Between Skills**  
- **Attack & Serve**: Strong positive correlation (**+0.77**), indicating players with strong attacks often excel in serves.  
- **Block & Receive**: Negative correlation (**-0.27**), suggesting blockers are less involved in receiving.  
- **Dig & Receive**: Strong positive correlation (**+0.62**), common for Liberos (L) who specialize in both.  
- **Age & Attack**: Weak negative correlation (**-0.18**), showing slight decline in attack performance with age.  

---

#### **5. Country-Level Analysis**  
- **Top 5 Countries by Average Attack**:  
  1. France: **6.67**   | 2. Japan: **6.60**   | 3. Cuba: **6.34**   | 4. Serbia: **6.00**   | 5. Italy: **5.97**  
- **Bottom 5 Countries by Average Attack**:  
  1. USA: **4.60**      | 2. Iran: **4.71**    | 3. Germany: **4.83** | 4. China: **5.09**    | 5. Brazil: **5.25**  
- **Total Digs (Top 3)**:  
  1. France: **38.59**  | 2. Italy: **35.89**  | 3. Slovenia: **33.85**  
- **Total Attack + Block (Top 3)**:  
  1. France: **70**     | 2. Japan: **68**     | 3. Cuba: **65**  

---

#### **6. Position-Specific Insights**  
- **Outside Hitters (OH)**:  
  - Highest average attack (**6.2**), led by Japan’s Ichikawa Yuki (15.80).  
  - Contribute significantly to receiving (**5.60** average for top OHs).  
- **Opposites (OP)**:  
  - Strong serves (**1.47** average), e.g., Nimir Abdel-Aziz (Serve: 2.08).  
- **Liberos (L)**:  
  - Zero attacking/blocking (role-specific), but excel in digs (e.g., Italy’s Fabio Balaso: **10.00 digs**).  
- **Setters (S)**:  
  - Highest set value: **26.89** (unspecified player).  

---

#### **7. Age-Driven Trends**  
- **Serving Performance**:  
  - **Best Age**: 31 years (**0.91 avg serve**).  
  - **Worst Age**: 41 years (0.00 serve, likely due to Libero role).  
- **Age Groups**:  
  - **[20–25]**: 0.53 avg serve | **[25–30]**: 0.66 | **[30–35]**: 0.43 | **[35–40]**: 0.27  
- **Decline in Serve**: Players over 35 show a sharp drop in serve performance.  

---

#### **8. Visualizations & Trends**  
- **Heatmap**: Confirmed strong Attack-Serve and Dig-Receive correlations.  
- **Scatter Plot (Block vs. Receive)**: Negative trend (**R = -0.27**), highlighting role specialization.  
- **Box Plot (Serve)**:  
  - **Median**: 0.42 | **IQR**: 0.24–0.76 | **Outliers**: Serves >1.5 (e.g., 2.08).  
- **Age Histogram**: 25–30 age group dominates (**~40 players**).  
- **Attack by Position**: OPs and OHs lead, while Liberos (L) have 0 attack.  

---

#### **9. Outliers & Notable Players**  
- **Nimir Abdel-Aziz (Nederland, OP)**: Highest serve (**2.08**) and 3rd-highest attack (**15.33**).  
- **Ichikawa Yuki (Japan, OH)**: Highest attack (**15.80**) and strong receive (**5.60**).  
- **Fabio Balaso (Italy, L)**: Top digs (**10.00**) and receive (**5.00**).  

---

####  **Methodology & Tools**  
- **Python Libraries**: `pandas` (data wrangling), `numpy` (statistics), `seaborn`/`matplotlib` (visualizations).  
- **Techniques**: Correlation analysis, grouped aggregations, histograms, heatmaps, and outlier detection.  
- **Data Source**: `VNL2023.csv` (cleaned, no duplicates or missing values).  

--- 

**Explore the code, visualizations, and interactive plots in the repository for deeper insights!**  
**Key Takeaway**: Attackers and servers peak in late 20s, while Liberos and Setters excel in defensive roles regardless of age.
