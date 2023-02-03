# Information-Retrieval-Using-Inverse-Index-
This program creates inverse indices for the terms present in the corpus and uses them to search for the relevant documents. 
The incidence matrix just creates a dictionary containing the unique terms as the keys and the list as values. The list has the ith element being 0 or 1 based on if the ith document
has the corresponding terms as the key.
But this approach is very inefficient and takes up a huge amount of memory to save the sparse lists.

Therefore we resort to inverse index approach where the keys still are the unique terms but the values are the doc ids where the key is present instead of 0s and 1s.
This reduces the size of the dictionary by a huge margin. Also nlks porter stemming is used to stem the words while saving so that a different version of the word still matches
with our query request.

Now when our query is made it is changed into its base word by stemming then comparisons are made for its presence in the term list. If the query matches then the corresponding
list is returned to be operated for complex query searches.

#hope this helps.
