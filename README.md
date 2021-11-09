{
   "nbformat": 4,
   "nbformat_minor": 5,
   "metadata": {
     "kernelspec": {
       "display_name": "Python 3",
       "language": "python",
       "name": "python3"
     },
     "language_info": {
       "codemirror_mode": {
         "name": "ipython",
         "version": 3
       },
       "file_extension": ".py",
       "mimetype": "text/x-python",
       "name": "python",
       "nbconvert_exporter": "python",
       "pygments_lexer": "ipython3",
       "version": "3.8.8"
     },
     "colab": {
       "name": "DataFrame.ipynb",
       "provenance": [],
       "include_colab_link": true
     }
   },
   "cells": [
     {
       "cell_type": "markdown",
       "metadata": {
         "id": "view-in-github",
         "colab_type": "text"
       },
       "source": [
         "<a href=\"https://colab.research.google.com/github/Chaturya3125/DAP/blob/main/DataFrame.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "353a21ab",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "96c972f8-1a3f-4307-8d7e-d6cedfcddbf6"
       },
       "source": [
         "import pandas as pd\n",
         "data = [1,2,3,4,5]\n",
         "df = pd.DataFrame(data)\n",
         "print (df)"
       ],
       "id": "353a21ab",
       "execution_count": 1,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "   0\n",
             "0  1\n",
             "1  2\n",
             "2  3\n",
             "3  4\n",
             "4  5\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "d67ef396",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "6d69afe2-f3c8-46b0-96cb-b2a9bfbb1447"
       },
       "source": [
         "import pandas as pd\n",
         "data = [['Alex',10],['Bob',12],['Clarke',13]]\n",
         "df = pd.DataFrame(data,columns=['Name','Age'])\n",
         "print (df)"
       ],
       "id": "d67ef396",
       "execution_count": 2,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "     Name  Age\n",
             "0    Alex   10\n",
             "1     Bob   12\n",
             "2  Clarke   13\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "cf661a2e",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "86450218-942a-44c0-a7a9-f00d22b19603"
       },
       "source": [
         "import pandas as pd\n",
         "data = [['Alex',10],['Bob',12],['Clarke',13]]\n",
         "df = pd.DataFrame(data,columns=['Name','Age'])\n",
         "print (df)"
       ],
       "id": "cf661a2e",
       "execution_count": 3,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "     Name  Age\n",
             "0    Alex   10\n",
             "1     Bob   12\n",
             "2  Clarke   13\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "e9423660",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "c92f8745-417d-4a5f-b78b-7a2f84c998a6"
       },
       "source": [
         "import pandas as pd\n",
         "data = {'Name':['Tom', 'Jack', 'Steve', 'Ricky'],'Age':[28,34,29,42]}\n",
         "df = pd.DataFrame(data)\n",
         "print (df)"
       ],
       "id": "e9423660",
       "execution_count": 4,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "    Name  Age\n",
             "0    Tom   28\n",
             "1   Jack   34\n",
             "2  Steve   29\n",
             "3  Ricky   42\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "6c3c4f87",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "1ad57fe9-732a-40bf-e737-2f6024765939"
       },
       "source": [
         "import pandas as pd\n",
         "data = {'Name':['Tom', 'Jack', 'Steve', 'Ricky'],'Age':[28,34,29,42]}\n",
         "df = pd.DataFrame(data, index=['rank1','rank2','rank3','rank4'])\n",
         "print (df)"
       ],
       "id": "6c3c4f87",
       "execution_count": 5,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "        Name  Age\n",
             "rank1    Tom   28\n",
             "rank2   Jack   34\n",
             "rank3  Steve   29\n",
             "rank4  Ricky   42\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "dee78c8f",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "de523921-3136-4648-aec6-18daa4c60ce7"
       },
       "source": [
         "import pandas as pd\n",
         "data = [{'a': 1, 'b': 2},{'a': 5, 'b': 10, 'c': 20}]\n",
         "df = pd.DataFrame(data)\n",
         "print (df)"
       ],
       "id": "dee78c8f",
       "execution_count": 6,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "   a   b     c\n",
             "0  1   2   NaN\n",
             "1  5  10  20.0\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "6fb8aa07",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "2c43b47d-5b44-4f83-f358-3a0d1ed251e4"
       },
       "source": [
         "import pandas as pd\n",
         "data = [{'a': 1, 'b': 2},{'a': 5, 'b': 10, 'c': 20}]\n",
         "\n",
         "#With two column indices, values same as dictionary keys\n",
         "df1 = pd.DataFrame(data, index=['first', 'second'], columns=['a', 'b'])\n",
         "\n",
         "#With two column indices with one index with other name\n",
         "df2 = pd.DataFrame(data, index=['first', 'second'], columns=['a', 'b1'])\n",
         "print (df1)\n",
         "print (df2)"
       ],
       "id": "6fb8aa07",
       "execution_count": 7,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "        a   b\n",
             "first   1   2\n",
             "second  5  10\n",
             "        a  b1\n",
             "first   1 NaN\n",
             "second  5 NaN\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "34a04b8d",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "e08fe1d0-b422-40cf-d0bd-7990f078898b"
       },
       "source": [
         "import pandas as pd\n",
         "\n",
         "d = {'one' : pd.Series([1, 2, 3], index=['a', 'b', 'c']),\n",
         "   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}\n",
         "\n",
         "df = pd.DataFrame(d)\n",
         "print (df)"
       ],
       "id": "34a04b8d",
       "execution_count": 8,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "   one  two\n",
             "a  1.0    1\n",
             "b  2.0    2\n",
             "c  3.0    3\n",
             "d  NaN    4\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "f9c6f323",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "c1b39445-6bf4-4810-9430-38232187ea13"
       },
       "source": [
         "#column selection\n",
         "\n",
         "import pandas as pd\n",
         "\n",
         "d = {'one' : pd.Series([10, 22, 32], index=['a', 'b', 'c']),\n",
         "   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}\n",
         "\n",
         "df = pd.DataFrame(d)\n",
         "print (df['one'])"
       ],
       "id": "f9c6f323",
       "execution_count": 9,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "a    10.0\n",
             "b    22.0\n",
             "c    32.0\n",
             "d     NaN\n",
             "Name: one, dtype: float64\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "db4d72d7",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "3a5531c9-2ae8-4001-cf11-bb9c36c12f96"
       },
       "source": [
         "#column selection\n",
         "#presence of NAN will convert int to float\n",
         "\n",
         "import pandas as pd\n",
         "\n",
         "de = {'one' : pd.Series([10, 22, 32,44], index=['a', 'b', 'c','d']),\n",
         "   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}\n",
         "\n",
         "\n",
         "df = pd.DataFrame(de)\n",
         "print (df['one'])"
       ],
       "id": "db4d72d7",
       "execution_count": 10,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "a    10\n",
             "b    22\n",
             "c    32\n",
             "d    44\n",
             "Name: one, dtype: int64\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "33ed2b90",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "b0db051d-dfba-4bfe-ed4b-2b13150349ca"
       },
       "source": [
         "# Adding a new column to an existing DataFrame object with column label by passing new series\n",
         "\n",
         "import pandas as pd\n",
         "\n",
         "d = {'one' : pd.Series([1, 2, 3], index=['a', 'b', 'c']),\n",
         "   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}\n",
         "\n",
         "df = pd.DataFrame(d)\n",
         "\n",
         "print (df)\n",
         "\n",
         "print (\"Adding a new column by passing as Series:\")\n",
         "df['three']=pd.Series([10,20,30],index=['a','b','c'])\n",
         "print (df)\n",
         "\n",
         "print (\"Adding a new column using the existing columns in DataFrame:\")\n",
         "df['four']=df['two']+df['three']\n",
         "\n",
         "print (df)"
       ],
       "id": "33ed2b90",
       "execution_count": 11,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "   one  two\n",
             "a  1.0    1\n",
             "b  2.0    2\n",
             "c  3.0    3\n",
             "d  NaN    4\n",
             "Adding a new column by passing as Series:\n",
             "   one  two  three\n",
             "a  1.0    1   10.0\n",
             "b  2.0    2   20.0\n",
             "c  3.0    3   30.0\n",
             "d  NaN    4    NaN\n",
             "Adding a new column using the existing columns in DataFrame:\n",
             "   one  two  three  four\n",
             "a  1.0    1   10.0  11.0\n",
             "b  2.0    2   20.0  22.0\n",
             "c  3.0    3   30.0  33.0\n",
             "d  NaN    4    NaN   NaN\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "39603ee5",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "f3016367-5d9a-4a41-b6f1-5cbf5f99846f"
       },
       "source": [
         "# Using the previous DataFrame, we will delete a column\n",
         "# using del function\n",
         "import pandas as pd\n",
         "\n",
         "d = {'one' : pd.Series([1, 2, 3], index=['a', 'b', 'c']), \n",
         "   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd']), \n",
         "   'three' : pd.Series([10,20,30], index=['a','b','c'])}\n",
         "\n",
         "df = pd.DataFrame(d)\n",
         "print (\"Our dataframe is:\")\n",
         "print (df)\n",
         "\n",
         "# using del function\n",
         "print (\"Deleting the first column using DEL function:\")\n",
         "del df['one']\n",
         "print (df)\n",
         "# using pop function\n",
         "print (\"Deleting another column using POP function:\")\n",
         "df.pop('two')\n",
         "print (df)"
       ],
       "id": "39603ee5",
       "execution_count": 12,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "Our dataframe is:\n",
             "   one  two  three\n",
             "a  1.0    1   10.0\n",
             "b  2.0    2   20.0\n",
             "c  3.0    3   30.0\n",
             "d  NaN    4    NaN\n",
             "Deleting the first column using DEL function:\n",
             "   two  three\n",
             "a    1   10.0\n",
             "b    2   20.0\n",
             "c    3   30.0\n",
             "d    4    NaN\n",
             "Deleting another column using POP function:\n",
             "   three\n",
             "a   10.0\n",
             "b   20.0\n",
             "c   30.0\n",
             "d    NaN\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "19e3bad2",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "6fcafdbb-90dc-4825-a59f-14a685697f28"
       },
       "source": [
         "#Selection by Label\n",
         "\n",
         "import pandas as pd\n",
         "\n",
         "d = {'one' : pd.Series([1, 2, 3], index=['a', 'b', 'c']), \n",
         "   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}\n",
         "\n",
         "df = pd.DataFrame(d)\n",
         "print (df.loc['b'])"
       ],
       "id": "19e3bad2",
       "execution_count": 13,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "one    2.0\n",
             "two    2.0\n",
             "Name: b, dtype: float64\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "ea9c30b4",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "7a61cb2d-6a66-4c62-cb0c-a1e444a898ba"
       },
       "source": [
         "#Selection by integer location\n",
         "\n",
         "import pandas as pd\n",
         "\n",
         "d = {'one' : pd.Series([1, 2, 3], index=['a', 'b', 'c']),\n",
         "   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}\n",
         "\n",
         "df = pd.DataFrame(d)\n",
         "print (df.iloc[2])"
       ],
       "id": "ea9c30b4",
       "execution_count": 14,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "one    3.0\n",
             "two    3.0\n",
             "Name: c, dtype: float64\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "92749649",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "bf217a4f-dc93-4099-e78b-79c92fdcc38c"
       },
       "source": [
         "#Slice Rows using : operator\n",
         "\n",
         "import pandas as pd\n",
         "\n",
         "d = {'one' : pd.Series([1, 2, 3], index=['a', 'b', 'c']), \n",
         "   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}\n",
         "\n",
         "df = pd.DataFrame(d)\n",
         "print (df[2:4])"
       ],
       "id": "92749649",
       "execution_count": 15,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "   one  two\n",
             "c  3.0    3\n",
             "d  NaN    4\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "4c96c886",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "13f4d892-d23a-4854-b287-a79f0c7baf3f"
       },
       "source": [
         "#Addition of Rows using append\n",
         "\n",
         "import pandas as pd\n",
         "\n",
         "df = pd.DataFrame([[1, 2], [3, 4]], columns = ['a','b'])\n",
         "df2 = pd.DataFrame([[5, 6], [7, 8]], columns = ['a','b'])\n",
         "print (df)\n",
         "print(\"after appending\")\n",
         "df = df.append(df2)\n",
         "print (df)"
       ],
       "id": "4c96c886",
       "execution_count": 16,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "   a  b\n",
             "0  1  2\n",
             "1  3  4\n",
             "after appending\n",
             "   a  b\n",
             "0  1  2\n",
             "1  3  4\n",
             "0  5  6\n",
             "1  7  8\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "f9d1ef83",
         "colab": {
           "base_uri": "https://localhost:8080/"
         },
         "outputId": "16698c99-0c32-45c3-af15-6e6c47d280ce"
       },
       "source": [
         "#Deletion of Rows\n",
         "\n",
         "import pandas as pd\n",
         "\n",
         "df = pd.DataFrame([[1, 2], [3, 4]], columns = ['a','b'])\n",
         "df2 = pd.DataFrame([[5, 6], [7, 8]], columns = ['a','b'])\n",
         "\n",
         "df = df.append(df2)\n",
         "\n",
         "# Drop rows with label 0\n",
         "df = df.drop(0)\n",
         "\n",
         "print (df)"
       ],
       "id": "f9d1ef83",
       "execution_count": 17,
       "outputs": [
         {
           "output_type": "stream",
           "name": "stdout",
           "text": [
             "   a  b\n",
             "1  3  4\n",
             "1  7  8\n"
           ]
         }
       ]
     },
     {
       "cell_type": "code",
       "metadata": {
         "id": "aa189a1a"
       },
       "source": [
         ""
       ],
       "id": "aa189a1a",
       "execution_count": null,
       "outputs": []
     }
   ]
