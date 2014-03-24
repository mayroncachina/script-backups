script-backups
==============

Scripts de backup que utilizo para sincronizar meu computador com Dropbox e Google Drive



- MAC
SymbolicLinker - http://seiryu.home.comcast.net/~seiryu/symboliclinker.html 


.bashrc

<code>
#### tmux shell init #### {
if [ $USER != root ]; then
    tmux_count=`tmux ls | wc -l`
    if [ "$tmux_count" == "0" ]; then
        tmux -2
    else
        if [ -z "$TMUX" ]; then
            if [ "$tmux_count" == "1" ]; then
                session_id=1
            else
                session_id=`echo $tmux_count`
            fi
        tmux -2 new-session -d -s $session_id
        tmux -2 attach-session -t $session_id
        fi
    fi
fi
#### tmux init end #### }
</code>
