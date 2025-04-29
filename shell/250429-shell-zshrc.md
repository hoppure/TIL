
## .zshrc 에 설정할 것
1. alias "python"="python3"
2. alias "vi"="vim" 
3. = 뒤에 띄어쓰지않기

## addition vimrc configuration
1. Vundle 을 이용하여 plugin설치하기
```shell
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

위 리포지토리를 클론하면 자동으로 깔림.

2. ~/.vimrc 에 다음 내용을 추가
```
"-----------------------------------------------------------------------"
" Vundle 환경설정
"------------------------------------------------------------------------"
filetype off                   " required!
set shell=/bin/bash
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
	" let Vundle manage Vundle
	" required! 
	Plugin 'VundleVim/Vundle.vim'

	" vim 하단에 파일 정보 띄우기
	Plugin 'vim-airline/vim-airline' 
	Plugin 'vim-airline/vim-airline-themes'
	" ...
call vundle#end()
filetype plugin indent on     " required!
	"
	" Brief help
	" :BundleList          - list configured bundles
	" :BundleInstall(!)    - install(update) bundles
	" :BundleSearch(!) foo - search(or refresh cache first) for foo
	" :BundleClean(!)      - confirm(or auto-approve) removal of unused bundles
	"
	" see :h vundle for more details or wiki for FAQ
	" NOTE: comments after Bundle command are not allowed..
```

3. vim을 다시 실행 시키고 command 모드에서 :PluginInstall 하면 플러그 인 들이 깔린다.

4. 각 플러그인 마다 ~/.vimrc 에서 설정할 수 있는 것이 있음. 
