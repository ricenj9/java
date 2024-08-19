
public class T1 {
	public static void main(String[] args) {
		int arr[][] = { { 2, 7, 6 }, { 9, 5, 1 }, { 4, 3, 8 } };
		boolean result = true;
		int sum = arr[0][0] + arr[1][1] + arr[2][2];// 计算一条斜边和
		if (sum != arr[0][2] + arr[1][1] + arr[2][0]) {
			result = false;
		} else {
			for (int x = 0; x < 3; x++) {
				// 计算行、列的和
				if (sum != arr[x][0] + arr[x][1] + arr[x][2] || sum != arr[0][x] + arr[1][x] + arr[2][x]) {
					result = false;
					break;
				}
			}
		}
		if (result) {
			System.out.println("数组行、列、对角线的和相等");
		} else {
			System.out.println("数组行、列、对角线的和不相等");
		}
	}
}


public class T2 {// 交换二维数组的行列数据
	public static void main(String[] args) {
		int i, j;// 定义两个变量，分别用来作为行和列的循环变量
		// 初始化一个静态的int型二维数组
		int[][] array = { { 8, 75, 23 }, { 21, 55, 34 }, { 15, 23, 20 } };
		System.out.println("—————原始数组—————");// 提示信息
		// 遍历原始的二维数组
		for (i = 0; i < 3; i++) {
			for (j = 0; j < 3; j++) {
				System.out.print(array[i][j] + "\t");// 输出原始数组中的元素
			}
			System.out.println();// 换行
		}
		int temp;// 临时变量
		// 通过循环调换元素的位置
		for (i = 0; i < 3; i++) {
			for (j = 0; j < i; j++) {
				temp = array[i][j];// 把数组元素赋给临时变量
				// 交换行列数据
				array[i][j] = array[j][i];
				array[j][i] = temp;
			}
		}
		System.out.println("——调换位置之后的数组——");// 提示信息
		// 遍历调换位置之后的二维数组
		for (i = 0; i < 3; i++) {
			for (j = 0; j < 3; j++) {
				System.out.print(array[i][j] + "\t");// 输出调换位置后的数组元素
			}
			System.out.println();// 换行
		}
	}
}

