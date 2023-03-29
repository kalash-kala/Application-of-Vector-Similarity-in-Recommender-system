# Application of Vector Similarity

### Intuition behind Recommender System :

- Using all the textual data we have such as title, overview, tagline and language, we can make use of TF-IDF vector representation to create vectors
- We will then also create a vector for the keywords are searching for, and then apply either ********************************Cosine Similarity******************************** or ************************************Euclidean Distance************************************ for calculating the similarity between the vectors
- Then sort the vectors based on the calculated value and there you have your top n recommendations

### Recap : Cosine Similarity

- In simple terms, it is the measure of the angle between the 2 vectors
- The lesser the angle, the more similar they are, hence their value or score should be more. This property is satisfied by $\cos\theta$, as angle increases, its value decreases
- In textual context, 0 implies no similarity ($90\degree$ angle) and 1 represents that they are pointing in same directions

### Recap : Euclidean Distance

- This is the sum of squares of differences of values of every dimension in 2 vectors
- This the most basic way of calculating the similarity
- The problem this faces is if the magnitude of either one of the vector is increased without changing its direction, then it will give a larger score, this doesn’t make sense as having more frequency of a word shouldn’t affect its similarity
- The above problem is taken care by normalising the vectors

### What to take for comparing the vectors :

- In TF-IDF, the vectors are normalised , so for comparison purposes both, Cosine Similarity and Euclidean Distance can be used as the score value holds no relevance here, the order of after sorting will remain same in both