# util.py

#各列の欠損値を表示する関数
def display_null_number(df):
  null_df=pd.DataFrame(df.isnull().sum().sort_values(ascending=False)).copy()
  null_df['null数']=null_df[0]
  display(null_df[['null数']][null_df['null数']>0])
