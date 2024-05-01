
import java.awt.*;
import java.awt.event.*;

public class JavaApplication3 extends Frame implements MouseListener {

    Label l;

    public JavaApplication3() {
        l = new Label();
        l.setBounds(25, 60, 250, 30);
        l.setAlignment(Label.CENTER);
        this.add(l);
        this.setSize(300, 300);
        this.setLayout(null);
        this.setVisible(true);
        this.addMouseListener(this);
        this.addWindowListener(new WindowAdapter() {
            public void windowClosing(WindowEvent e) {
                dispose();
            }
        });
    }

    public void mouseClicked(MouseEvent e) {
        l.setText("Mouse Clicked");
    }

    public void mousePressed(MouseEvent e) {
    }

    public void mouseReleased(MouseEvent e) {
    }

    public void mouseEntered(MouseEvent e) {
        l.setText("Mouse Entered");
    }

    public void mouseExited(MouseEvent e) {
        l.setText("Mouse Exited");
    }

    public static void main(String[] args) {
        new JavaApplication3();
    }
}
