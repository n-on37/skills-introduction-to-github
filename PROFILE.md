#include <iostream>
using namespace std;
class myVector{
    private:
    int size_;
    int capacity_;
    int *data;
    public:
    myVector();                  // 默认构造函数
    myVector(int *vecotr_p);    // 数组构造vicitor
    myVector(const myVector &vec); // 复制拷贝构造函数
    ~myVector();                 // 析构函数
    // 功能函数声明
    int empty();
    int capacity();
    int size();
    int pop();
    void push(int item);
    int at( int index);
    int *reserve();
    int *delete_size();
    void swap(int index1, int index2);
    void insert_array(int index, int *p);
    void delete_array(int index, int *p);
    // 运算符重载（成员函数类）
    myVector operator+(myVector &v);
    myVector operator=(const myVector &vec);
    int operator[](int);
    int operator++();
    friend istream &operator>>(istream &input, myVector &v);
    friend ostream &operator<<(ostream &output, myVector &v);
};
// 运算符重载（友元类）
 // 存在问题
istream &operator>>(istream &input, myVector &v);
ostream &operator<<(ostream &output, myVector &v);
