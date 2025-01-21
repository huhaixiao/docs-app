# chmod

- change mode
- drwxrwxrwx
- u -> user
- g -> group
- o -> other

```shell
# change file mode
sudo chmod -R 777 dir
# add rwx for user
chmod -R u+rwx dir
# add rwx for group
chmod -R g+rwx dir
# remove rwx for other user
chmod -R o-rwx dir
```
