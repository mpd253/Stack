# Stack

import java.util.Scanner;  
import java.util.Stack;

'''python
public class Stack0603 {							// 후입선출 LIFO(Last In First Out) stack
'''	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Stack<Integer> stack = new Stack<Integer>();
		Scanner scanner = new Scanner(System.in);
		
		int num = scanner.nextInt();
		
		for(int i = 0; i < num; i++) {
			String some = scanner.next();
			if(some.equals("push")) {
				int somenum = scanner.nextInt();
				stack.push(somenum);
			} else if(some.equals("pop")) {			// 스택에서 가장 위에 있는 정수를 빼고 그 수를 출력
				if(stack.isEmpty()) {
					System.out.println("-1");		// 스택에 들어있는 정수가 없으면 -1을 출력
				} else {
					System.out.println(stack.pop());	// 스택에 들어있는 정수가 있으면 가장 위에 있는 정수를 빼고 그 수를 출력
				}
			} else if(some.equals("size")) {			
				System.out.println(stack.size());	// 스택에 들어있는 정수의 개수를 출력
			} else if(some.equals("empty")) {
				if(stack.isEmpty()) {
					System.out.println("1");		// 스택이 비어있으면 1 출력
				} else {
					System.out.println("0");		// 스택이 비어있지 않으면 0 출력
				}
			} else if(some.equals("top")) {
				if(stack.isEmpty()) {
					System.out.println("-1");		// 스택에 들어있는 정수가 없다면 -1을 출력
				} else {
					System.out.println(stack.peek());	// 스택에 들어있는 정수가 있다면 스택의 가장 위에 있는 정수를 출력 (삭제x)
				}
			}
		}
	}
}
