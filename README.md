# FileProjrct
FileWriter and FileRider
<br>
package com.edubridge;

import java.io.*;
import java.util.Scanner;

public class FileProject {

	public static void main(String[] args) {
		File f=new File("c:/file_edubridge/projectfile.text");

		
		try {
			FileWriter fw = new FileWriter(f);
			BufferedWriter bw=new BufferedWriter(fw);
			Scanner sc=new Scanner(System.in);
			System.out.println("enter your data");
			bw.write(sc.nextLine()+"\n");
			bw.write(sc.nextLine());
			bw.flush();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
         
         try {
			FileReader fr=new FileReader(f);
			BufferedReader br=new BufferedReader(fr);
			try {
				String data=br.readLine();
				System.out.println(data);
				while(data!=null)
				{
					data=br.readLine();
					System.out.println(data);
				}
				

			} catch (IOException e) {
				// TODO Auto-generated catch block
				e.printStackTrace();
			}
			
		} catch (FileNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
         
         
	}

}

