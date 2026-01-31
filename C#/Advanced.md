
# 1.  What is the difference between IEnumerable and IQueryable?
IEnumerable	IQueryable
Executes in memory	Executes in database
Used for collections	Used for LINQ to SQL
Less efficient for large data	More efficient
# 2 Dictionary
// Creating a dictionary
        Dictionary<int, string> sub = new Dictionary<int, string>();

        // Adding elements
        sub.Add(1, "C#");
        sub.Add(2, "Javascript");
        sub.Add(3, "Dart");

        // Displaying dictionary
        foreach (var ele in sub){
            Console.WriteLine($"Key: {ele.Key}, Value: {ele.Value}")
            
