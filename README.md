# daneel_utilities

使用前请先修改sub_script_head, sub_script_head_py, sub_script_head_gpu中的zlsong为自己账户名

将daneel_utilities文件传入目录，vim ~/.bashrc，添加export PATH=<daneel_utilities文件夹绝对路径>:$PATH，:wq保存后，source ~/.bashrc

sub_vasp ------ 自动批量提交VASP任务，结构优化任务自动纠错(机器学习小组)，具体使用运行sub_vasp -h查看

sub_program ------ 提交程序任务到wang队列(修改队列可修改sub_script_head_py文件)，使用示例：sub_python "python ..."，或写一个文件名为command_file，里面写入程序命令，然后输入sub_python

sub_gpu ------ 提交程序任务到GPU节点(修改GPU数量可修改sub_script_head_gpu文件)，使用示例：sub_gpu "python ..."，或写一个文件名为command_file，里面写入程序命令，然后输入sub_gpu

check_energy ------ 查看VASP优化任务结果，得到能量随离子步变化关系

check_relax ------ 查看VASP优化任务结果，得到能量随离子步变化关系，最大力随离子步变化关系，最后几个离子步最大力的变化，结构均方位移随离子步变化关系

check_VASP_job_status ------ 查看当前目录下(包括任意数量子目录)所有VASP任务运行情况

