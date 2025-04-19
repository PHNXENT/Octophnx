// Preferred way using 'using' statement
using (StreamReader sr = File.OpenText("data.txt"))
{
    // Use the StreamReader object
} // sr.Dispose() is automatically called here

// Equivalent using try-finally
StreamReader sr = null;
try
{
    sr = File.OpenText("data.txt");
    // Use the StreamReader object
}
finally
{
    if (sr!= null)
    {
        sr.Dispose();
    }
}
