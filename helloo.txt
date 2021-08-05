help(){
echo "run this script as below"
echo "./hello.sh file_path"
}

if [[ $# -lt 1 || $# -gt 1 ]]; then 
help
exit 1
fi

if [[ -e $1 ]]; then
echo "file is present"
else
echo "given file does not exist or file name is wrong"
exit 1
fi

echo "File to be modified $1"
echo "Hello World" >> $1