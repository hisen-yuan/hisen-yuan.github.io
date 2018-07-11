---
title: Java三种创建对象的方式
tags: [java,对象]
date: 2017-02-10 22:30:19
categories: java
---
有一个实现了Cloneable接口的Person类
输出：

```
<使用new关键字创建对象>
hisen已成年
体重为：50
年龄为：23
<使用newInstance()方法创建对象>
体重为：0
年龄为：0
<使用clone()方法创建对象>
hisen已成年
体重为：50
年龄为：23
```

具体实现：
<!--more-->
```+java
package com.hisen.javaGaiShu.page73test5;

/**
 * 三种方式创建对象
 * 
 * @author hisenyuan 2017年2月10日 下午10:27:14
 */
public class Person implements Cloneable {
	private String name;
	private int weight;
	private int age;

	public Person() {
	}

	public Person(String name, int weight, int age) {
		super();
		this.name = name;
		this.weight = weight;
		this.age = age;
	}

	public void young() {
		if (age >= 18 && age <= 100)
			System.out.println(name + "已成年");
		if (age > 0 && age < 18)
			System.out.println(name + "未成年");
	}

	@Override
	public String toString() {
		return "体重为：" + weight + "\n年龄为：" + age;
	}

	public static void main(String[] args) throws Exception {
		System.out.println("<使用new关键字创建对象>");
		Person p1 = new Person("hisen", 50, 23);
		p1.young();
		System.out.println(p1);

		System.out.println("<使用newInstance()方法创建对象>");
		Class c = Class.forName("com.hisen.javaGaiShu.page73test5.Person");
		Person p2 = (Person) c.newInstance();
		p2.young();
		System.out.println(p2);

		System.out.println("<使用clone()方法创建对象>");
		Person p3 = (Person) p1.clone();
		p3.young();
		System.out.println(p3);
	}

}

```
