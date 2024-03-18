# -1
用于日常练习python，便于检查和自测
1. 给定一个整数数组 nums 和一个整数目标值 target，请你在该数组中找出 和为目标值 target  的那 两个 整数，并返回它们的数组下标。

你可以假设每种输入只会对应一个答案。但是，数组中同一个元素在答案里不能重复出现。

你可以按任意顺序返回答案。

def two_sum(nums,target): #定义一个函数two_sum，函数接受了两个参数nums,target
    num_dict={}#创建了一个空字典num_dict，用于存储数组中的数字及下标
    for i, num in enumerate(nums): #使用enumerate函数遍历数组nums，同时获取数字的下标i和对应的值num
        complement=target-num #计算目标值target与当前数字num的差值，用于检查是否存在与当前数字相加等于目标值的另一个数字
        if complement in num_dict:#检查差值 complement是否在 num_dict中，如果在，说明找到了两个数的和等于目标值
            return [num_dict[complement],i]#如果找到两个数的和等于目标值，返回这两个数的下标，其中[num_dict[complement],i]是第一个数的下标，i是的二个数的下标
        num_dict[num]=i#将当前数字num及其下标i存入 num_dict中，以便后续查找与当前数字相加等于目标值的另一个数字的下标
nums=[2,7,11,15]#定义了一个整数数组nums
target=9#定义了一个目标值target
result=two_sum(nums,target)#调用two_sum函数，并将返回的结果存储在result变量中
print(result)
