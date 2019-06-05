using System.Linq;
using System.Text;
using System.Threading.Tasks;
using ConsoleApp12;
using NUnit.Framework;

namespace ClassLibrary1

{
    [TestFixture]
    class assignment
    {
      //  public TriangleSolver t = new TriangleSolver();

        [Test]
        public void Analyze_input10_input10_input10_ExpectedGivenDimensionsformaEquilateralTriangle()
        {
            //Arrange
            int a = 10;
            int b = 10;
            int c = 10;
            string expected = "Given Dimensions form a Equilateral Triangle";
            TriangleSolver.Analyze(a, b, c);

            //Act

