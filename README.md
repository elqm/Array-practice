# Array-practice

	package com.greedy.section01.array.level02.normal;

	import java.util.Scanner;

	public class Application2 {

	public static void main(String[] args) {
		
		/* 주민등록번호를 스캐너로 입력 받고 문자 배열로 저장한 뒤,
		 * 성별 자리 이후부터 *로 가려서 출력하세요
		 * 
		 * -- 입력 예시 --
		 * 주민등록번호를 입력하세요 : 990101-1234567
		 * 
		 * -- 출력 예시 --
		 * 990101-1******
		 */
		
		Scanner sc = new Scanner(System.in);
		System.out.print("주민등록번호를 입력하세요 : ");
		String num = sc.nextLine();
		
		char[] arr = new char[num.length()];
		for(int i = 0; i < num.length(); i++) {
			arr[i] = num.charAt(i);
			
	//			if(i > 7) {
	//				arr[i] = '*';
	//			}
		}
		
		for(int i = 0; i < 8; i++) {
			System.out.print(arr[i]);
		}
		for(int i = 8; i < arr.length; i++) {
			System.out.print('*');
		}
		
		
	//		System.out.println(arr);
		
		
	}

	}



	package com.greedy.section01.array.level02.normal;

	import java.util.Scanner;

	public class Application1 {

	public static void main(String[] args) {
		
		/* 문자열을 하나 입력받아 문자 자료형 배열로 바꾼 뒤
		 * 검색할 문자를 하나 입력 받아 
		 * 입력 받은 검색할 문자가 문자열에 몇개 있는지를 출력하세요
		 * 
		 * -- 입력 예시 --
		 * 문자열을 하나 입력하세요 : helloworld
		 * 검색할 문자를 입력하세요 : l
		 * 
		 * -- 출력 예시 --
		 * 입력하신 문자열 helloworld에서 찾으시는 문자 l은 3개 입니다.
		 * */
		
		Scanner sc = new Scanner(System.in);
		System.out.print("문자열을 하나 입력하세요 : ");
		String str = sc.nextLine();
		
		char[] a = new char[str.length()];
		for(int i = 0; i < str.length(); i++) {
			a[i] = str.charAt(i);
		}
		
		System.out.print("검색할 문자를 입력하세요 : ");
		char ch = sc.nextLine().charAt(0);
		
		int count = 0;
		
		for(int i = 0; i < a.length; i++) {
			if(a[i] == ch) {
				count++;
			}
		}
		
		System.out.println("입력하신 문자열 " + str + "에서 찾으시는 문자 " + ch + "은 " + count + "입니다.");
		
		
		
		
	}

	}
