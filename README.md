# AdaTsang.github.io

##  算法
* 特征
  1.  有穷性
  2.  确定性
  3.  可行性
  4.  输入
  5.  输出

* 设计衡量
  1.  正确性
  2.  可读性
  3.  健壮性
  4.  时间复杂度
  5.  空间复杂度

* 基本分类
  1.  快速排序
  2.  堆排序
  3.  归并
  4.  二分查找
  5.  线性查找
  6.  深度优先
  7.  广度优先
  8.  戴克斯特拉
  9.  动态规划
  10. 贝叶斯分类

* 基本算法
  1.  冒泡排序
      ```javascript
          function bubbleSort(arr) {
            var len = arr.length;
            for(var i = 0; i < len - 1; i++) {
              for(var j = 0; j < len - 1 - i; j ++) {
                if(arr[j] > arr[j+1]) {
                  [arr[j], arr[j+1]] = [arr[j+1], arr[j]] // 交换位置
                }
              }
            }
          }
      ```

* 算法面试题
    1.  两数之和 - 给定一个整数数组nums和一个目标值target，请你在该数组中找出和为目标值的那**两个**整数，并返回他们的数组**下标**。
    ```javascript
        // nums = [2, 7, 11, 15], target = 9
        let sum = function(nums, target) {
          let map = new Map();
          for(let i = 0; i < nums.lengths; i++) {
            let r = target - nums[i];
            if(map.has(k)) {
              return [map.get[k], i]
            }
            map.set(nums[i], i)
          }
        }
        return [];
    ```
    2.  给定一个排序数组，你需要在**原**删除重复出现的元素，使得每个元素只出现一次，返回移除后数组的新长度。
        不要使用额外的数组空间，你必须在 原地 修改输入数组 并在使用 O(1) 额外空间的条件下完成。
    ```javascript
        /*
        *给定数组 nums = [1,1,2], 
        *函数应该返回新的长度 2, 并且原数组 nums 的前两个元素被修改为 1, 2。 
        *不需要考虑数组中超出新长度后面的元素
        */
        var removeDuplicates = function(nums) {
          if(nums.length < 2) return nums.length
          var i = 0;
          for(var j = 1; j < nums.length; j++) {
              if(nums[i] !== nums[j]) {
                  i++;
                  nums[i] = nums[j]
              } 
          }
          return i+1;
        };
    ```
      
