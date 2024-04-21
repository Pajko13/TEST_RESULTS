# TEST_RESULTS
Osnovne operacije su uredu(+,*,/,-)

Redosled operacija je uredu

Kod deljenja sa nulom javra gresku 

Uspesno racunanje u ekstremnim uslovima primer:(999999999*999999999)

Kada pokusam da podelim 1/0 u terminalu ne izbacuje nikakvu gresku

Kada ukucam dva operatora za redom prijavljuje gresku 

Ako umesto operatora mnozenja(*) pomesamo sa (x) dobijam gresku
..............................................................................
JEDINICNI TEST
import static org.junit.Assert.assertEquals;
import org.junit.Test;

public class CalculatorTest {

    @Test
    public void testCalculate() {
        // Testiramo metodu Calculate sa jednostavnim izrazom: 2 + 3 * 4
        // Očekivani rezultat je 14

        // Priprema ulaznih podataka
        List<Float> numbers = new ArrayList<>();
        numbers.add(2f);
        numbers.add(3f);
        numbers.add(4f);

        List<String> operations = new ArrayList<>();
        operations.add("+");
        operations.add("*");

        // Poziv metode koju testiramo
        Calculator.Calculate(numbers, operations);

        // Provera očekivanog rezultata
        assertEquals(14f, Calculator.finalResult, 0.001); // Koristimo delta parametar za toleranciju float tačnosti
    }
}
