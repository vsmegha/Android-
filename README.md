package com.example.android.justjava;
        import android.os.Bundle;
        import androidx.appcompat.app.AppCompatActivity;
        import android.view.View;
        import android.widget.TextView;
        import java.text.NumberFormat;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    /**
     * This method is called when the order button is clicked.
     */
    public void submitOrder(View view) {
        int quantity=3;
        display(quantity);
        displayPrice(quantity*5);
    }
    public void increment(View view) {
        int quantity = 3;
        display(quantity);
    }
    public void decrement(View view) {
        int quantity=1;
        display(quantity);}
    /**
     * This method displays the given quantity value on the screen.
     */
    private void display(int number) {
        TextView quantityTextView = (TextView) findViewById(R.id.nameview);
        quantityTextView.setText("" + number);
    }/**
     * This method displays the given price on the screen.
     */
    private void displayPrice(int number) {
        TextView priceTextView = (TextView) findViewById(R.id.amt_text_view);
        priceTextView.setText(NumberFormat.getCurrencyInstance().format(number));
    }
}
