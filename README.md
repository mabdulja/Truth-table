# table panel
truth table program

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import javax.swing.event.*;

public class TablePanel extends JPanel {

	private int width, height;
	private JTextField one;
	private JPanel main, top, bottom, sub, command;
	private JButton enter, reset, back, p, q, r, neg, or ,and, imp, parenth;
	private JTextArea eq;
	
	public TablePanel()
	{
		
		//command buttons 
		one = new JTextField();
		enter = new JButton("Enter");
		enter.addActionListener(new ButtonListener());
		reset = new JButton("Reset");
		reset.addActionListener(new ButtonListener());
		eq = new JTextArea(one.getText());
		p = new JButton("p");
		p.addActionListener(new ButtonListener());
		q = new JButton("q");
		q.addActionListener(new ButtonListener());
		r = new JButton("r");
		r.addActionListener(new ButtonListener());
		neg = new JButton("~");
		neg.addActionListener(new ButtonListener());
		or = new JButton("v");
		or.addActionListener(new ButtonListener());
		and = new JButton("^");
		and.addActionListener(new ButtonListener());
		imp = new JButton("->");
		imp.addActionListener(new ButtonListener());
		parenth = new JButton("()");
		parenth.addActionListener(new ButtonListener());
		back = new JButton("backspace");
		back.addActionListener(new ButtonListener());
		
		command = new JPanel(new GridLayout(2,4));
		command.add(neg);
		command.add(p);
		command.add(q);
		command.add(r);
		command.add(parenth);
		command.add(and);
		command.add(or);
		command.add(imp);
		
		
		//sub panel consists of the text field, enter and reset buttons
		sub = new JPanel();
		sub.setLayout(new GridLayout(1,3));
		sub.add(enter);
		sub.add(back);
		sub.add(reset);
		
		//top panel consists of sub and text area
		top = new JPanel(new GridLayout(3,1));
		top.add(eq);
		top.add(command);
		top.add(sub);
	
		
		//bottom panel consists of the generated truth table from the top panel
		bottom = new JPanel(new GridLayout(1,4));
		
		//main panel, combination of top and bottom panel
		main = new JPanel();
		main.setLayout(new GridLayout(2,1));
		main.add(top);
		main.add(bottom);
		add(main);
	}
	
	private class ButtonListener implements ActionListener
	{
		public void actionPerformed(ActionEvent event)
		{
			JButton buttonX = (JButton) event.getSource();
			
			
			

			}
		
	}
	
	
}
