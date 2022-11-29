# ogrenci sayisini ve notunu yazdırıp kalıp kalmadığını ifade eden program



internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("sınıftaki öğrenci sayısını giriniz");
            int ogrncs = Convert.ToInt32(Console.ReadLine());  
            string[] isimler = new string[ogrncs];
            byte[] notlar = new byte[ogrncs];
            int gecenler = 0;
            int kalanlar = 0;

            for (int i = 0; i < isimler.Length; i++)
            {
                Console.WriteLine((i+1) + ". Öğrencinin adını giriniz.");
                isimler[i] = Console.ReadLine();
                Console.WriteLine((i+1) + ". Öğrencinin notunu giriniz.");
                notlar[i] = Convert.ToByte(Console.ReadLine());
            }

            for(int i = 0; i < isimler.Length; i++)
            {
                if (notlar[i] >= 50)
                {
                    Console.WriteLine(isimler[i] + $" isimli öğrencinin NTP dersinden {notlar[i]} puan ile geçti");
                    gecenler++;
                    
                }
                else if (notlar[i] <= 50)
                {
                    Console.WriteLine(isimler[i] + $" isimli öğrencinin NTP dersinden {notlar[i]} puan ile kaldı");
                    kalanlar++;
                    
                }
   
            }
            Console.WriteLine(gecenler + " Kişi geçti");
            Console.WriteLine(kalanlar + " Kişi kaldı");

            Console.ReadKey();


        }
    }
}
