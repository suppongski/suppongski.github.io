---
layout: post
title: 3주차 과제 (선택정렬)
subtitle: 선택정렬 문제 포스트하여 링크
categories: 과제
tags: [과제, 정렬]
---
## 선택정렬
* 선택정렬이란 주어진 배열 중 랜덤으로 하나의 수를 피봇으로 선택하여 나머지 수 들을 피봇보다 작으면 왼쪽, 피봇보다 크면 오른쪽으로 나누고, 피봇의 왼쪽과 오른쪽 에 대하여 각각 피봇을 선정하여 다시 나누어 가는 정렬 방법이다.
---
# 나만의 예제
* 배열의 크기와 배열을 입력하고 원하는 n번째로 작은 숫자를 찾아내는 문제이다.
```
import java.util.Scanner;
import java.util.Random;
public class week3_selection {
    public static int selection(int size, int arr[], int find) {
        Random random = new Random();
        int lcount = 0, rcount = 0;
        int p = random.nextInt(size);
        int temp = arr[0];
        arr[0] = arr[p];
        arr[p] = temp;
        int left[] = new int[size];
        int right[] = new int[size];
        for (int a=1; a<size; a++)
        {
            if (arr[a] < arr[0])
            {
                left[lcount] = arr[a];
                lcount++;
            }
            else
            {
                right[rcount] = arr[a];
                rcount++;
            }
        }
        if (find == lcount+1)
        {
            return arr[0];
        }
        else if (find <= lcount)
        {
            return selection(lcount, left, find);
        }
        else
        {
            return selection(rcount, right, find-(lcount+1));
        }

    }





    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int array[];
        System.out.println("배열의 크기를 입력: ");
        int n = scanner.nextInt();
        array = new int[n];
        System.out.println("배열을 입력: ");
        for (int i=0; i<n; i++)
        {
            array[i] = scanner.nextInt();
        }
        System.out.println("몇번째 작은 수를 구할까요?: ");
        int k = scanner.nextInt();

        int result = selection(n, array, k);
        System.out.println(k + "번째 작은 수는 : " + result);

        scanner.close();
    }
}
```
---
## INTELLIJ 콘솔창 한글깨짐 해결방법
1. "edit configurations..."를 열어 open jdk-17 로 변경해 준다.