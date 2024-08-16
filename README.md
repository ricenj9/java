public class T1 {
	public static void main(String[] args) {
		int count = 0;
		for (int i = 1; i < 101; i++) {
			// 默认是素数
			boolean flag = true;
			for (int j = 2; j <= Math.sqrt(i); j++) {
				if (i % j == 0) {
					// 能整除
					flag = false;
				}
			}
			if (flag) {
				count += 1;
				System.out.print(i + ",");
			}
		}
		System.out.println("\n共计" + count + "个素数");
	}
}

public class T2 {
	public static void main(String[] args) {
		int year = 2021;//年份
		switch (year % 12) {
		case 0:
			System.out.println(year + "年的生肖是猴");
			break;
		case 1:
			System.out.println(year + "年的生肖是鸡");
			break;
		case 2:
			System.out.println(year + "年的生肖是狗");
			break;
		case 3:
			System.out.println(year + "年的生肖是猪");
			break;
		case 4:
			System.out.println(year + "年的生肖是鼠");
			break;
		case 5:
			System.out.println(year + "年的生肖是牛");
			break;
		case 6:
			System.out.println(year + "年的生肖是虎");
			break;
		case 7:
			System.out.println(year + "年的生肖是兔");
			break;
		case 8:
			System.out.println(year + "年的生肖是龙");
			break;
		case 9:
			System.out.println(year + "年的生肖是蛇");
			break;
		case 10:
			System.out.println(year + "年的生肖是马");
			break;
		case 11:
			System.out.println(year + "年的生肖是羊");
			break;
		}
	}
}


public class T3 {
	public static void main(String[] args) {
		int centigrade = -40; // 摄氏度的初始值为-40
		double fahrenheit; // 华氏度
		do {
			centigrade += 10; // 每行间隔10度
			fahrenheit = centigrade * 9 / 5.0 + 32; // 由摄氏度转为华氏度的公式
			System.out.println("摄氏温度：" + centigrade + "℃\t华氏温度：" + fahrenheit + "ㄈ");
		} while (centigrade < 50);
	}
}
