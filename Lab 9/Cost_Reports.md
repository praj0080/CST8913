import pandas as pd

# Load the exported CSV file
csv_file_path = "/mnt/data/cost-analysis.csv"
df = pd.read_csv(csv_file_path)

# Display the first few rows to understand the structure
df.head()
