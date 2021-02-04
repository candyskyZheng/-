

import os,sys
import re

def rename_zuozhe(old_name , new_name_zuozhe):
	try:
		last_name = old_name.split(", et al.,")[0].split(" ")[0]
		first_name = old_name.split(", et al.,")[0].split(" ")[1:]
		name = last_name + ', ' + first_name[0][0].upper() + '.'
		if "," in last_name:
			new_name_zuozhe = old_name
			return new_name_zuozhe
		else:
			new_name_zuozhe = old_name.replace(old_name.split(", et al.,")[0] , name)
			os.rename(os.path.join(path,old_name),os.path.join(path,new_name_zuozhe))
			return new_name_zuozhe
	except Exception as e:
		pass


def rename_subfolders0():
	old_names = os.listdir(path)
	for old_name in old_names:
		if old_name != sys.argv[0] and "et al.," in old_name:
			new_name_zuozhe = ''
			rename_zuozhe(old_name , new_name_zuozhe)

if __name__ == '__main__':
	path0 = r'D:\文件更新\Refer_Update0203'
	path1 = os.listdir(path0)
	for path2 in path1:
		path = r'D:\文件更新\Refer_Update0203\\A.J. Bermudez folder'
		path = path.replace(path.split("Refer_Update0203\\")[1] , path2)
		print(path)
		rename_subfolders0()
		

