# DAO Data Analysis: Governance and Operational Efficiency in DAOs

This project involves analyzing governance and operational efficiency in Decentralized Autonomous Organizations (DAOs) using data collected from various blockchain platforms such as Snapshot, Polygonscan, and Etherscan. The primary objective is to explore how DAOs manage decision-making and participation, and to identify key trends in governance structures using data management techniques.

## Project Overview

- **Objective**: To analyze the operational and governance efficiency in DAOs by cleaning, structuring, and analyzing blockchain data from 15 DAOs.
- **Key Methods**: Data cleaning, restructuring, database design using MongoDB, and analysis of governance dynamics, including voting behavior, proposal activity, and community engagement.
- **Tech Stack**: Python, MongoDB, Pandas, Matplotlib, and PyMongo.

## Dataset

The dataset contains information from 15 DAOs, focusing on governance activities such as proposals, votes, treasury management, and participation data. The data was collected from Snapshot, Polygonscan, and Etherscan platforms.

### Dataset Features:
- `DAOs`: General information about each DAO (name, network, website, voting strategies).
- `Proposals`: Detailed information about governance proposals made within DAOs.
- `Votes`: Voting activity on the proposals.
- `Follows`: Data on community engagement and members following each DAO.
- `Treasury`: Addresses and balances of DAO treasuries.

### File Structure:
- **`Code.ipynb`**: Jupyter notebook containing the code for loading, cleaning, and processing DAO data from various sources.
- **`Code.pdf`**: PDF version of the code for easy viewing.
- **`Report.pdf`**: Detailed report discussing the methodology, results, and conclusions from the DAO governance analysis.
- **`requirements.txt`**: Python dependencies required to run the project.

## Data Processing Steps

1. **Data Loading**:
   - Data from various pickle files (including `Snapshot`, `Polygonscan`, and `Etherscan`) were loaded into MongoDB collections.
   - Large integers in the data were converted to strings to ensure compatibility with MongoDB’s storage capabilities.

2. **Data Cleaning and Structuring**:
   - Created separate MongoDB collections for DAOs, proposals, votes, follows, treasuries, and strategies.
   - Cleaned each collection by removing null or redundant fields, normalizing data (e.g., converting addresses to lowercase), and handling large numerical values.
   - Unnested nested data structures to simplify access and querying.

3. **Community Engagement Analysis**:
   - Analyzed community engagement by assessing the number of follows, proposals, and votes for each DAO.
   - Performed clustering analysis to identify trends in voting behavior and proposal activity across different DAOs.

4. **Governance Structure Analysis**:
   - Investigated the distribution of voting power, participation dynamics between members and admins, and the most common voting strategies across DAOs.

## Key Results

### 1. DAO Popularity and Engagement:
   - **Most Followed DAOs**: DAOs like `Uniswap` and `Aave` had the largest number of community members following their governance activities, indicating their influence within the blockchain ecosystem.
   - **Voting Behavior**: DAOs with high numbers of proposals (e.g., `Arbitrum Foundation`) exhibited active governance, with many community members participating in votes.

### 2. Centralization of Voting Power:
   - The analysis showed a concentration of voting power within a small number of participants in most DAOs, indicating a potential risk of centralization in governance.

### 3. Gas Fee Analysis:
   - **Gas Fees**: Significant differences in gas fees were observed between the `Ether` and `Polygon` networks, with Polygon having higher average fees per transaction.

## Usage

The Jupyter notebook demonstrates the following:
1. **Data Loading**: Loading data from pickle files into MongoDB collections.
2. **Data Preprocessing**: Cleaning and structuring DAO-level data, including normalization, removing duplicates, and unnesting nested structures.
3. **DAO Governance Analysis**: Analyzing DAO popularity, community engagement, voting behavior, and operational efficiency.
4. **Visualization**: Generating visual insights using `Matplotlib` to better understand the governance dynamics within DAOs.

## Installation

To run the project locally:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/DAO-Data-Analysis.git
    cd DAO-Data-Analysis
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the Jupyter notebook:
    ```bash
    jupyter notebook
    ```

## Acknowledgements

This project was developed as part of the MSc in Business Analytics at Bayes Business School.

## License

MIT License
