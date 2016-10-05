# Hello-world
firstattempt on github
//sample code
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
            List<Car> myCar = new List<Car>()
          {
              new Car() {VIN =123, make="maruthi",model="aulto",strickerPrice=3000,year=2010},
              new Car() {VIN =123, make="maruthi",model="swift",strickerPrice=35000,year=2015},
              new Car() {VIN =123, make="Honda",model="CR-v",strickerPrice=1000000,year=2015},
              new Car() {VIN =123, make="maruthi",model="800",strickerPrice=2000,year=1999},
              new Car() {VIN =123, make="Toyota",model="Innova",strickerPrice=185000,year=2013},
              new Car() {VIN =123, make="Mahindra",model="XUV-500",strickerPrice=350000,year=2010},
          };

            var _car = from car in myCar

                       where car.make == "maruthi"
                       select car;
            foreach (var car in _car)
            {
                Console.WriteLine("{0} {1}", car.model, car.strickerPrice);
            }
            Console.ReadLine();
        }
    }

    class Car
    {
        public int VIN { get; set; }
        public string make { get; set; }
        public string model { get; set; }
        public decimal strickerPrice { get; set; }
        public int year { get; set; }
    }
 }
