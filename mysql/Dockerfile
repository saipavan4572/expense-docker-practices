FROM mysql:8.0
RUN adduser -r expense
# system user, no login (not a human) -- in Debian OS

ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1 \
    MYSQL_USER=expense \
    MYSQL_PASSWORD=ExpenseApp@1 \
    MYSQL_DATABASE=transactions
RUN chown -R expense:expense /var/lib/mysql /var/run/mysqld
# changing the ownership of /var/lib/mysql, /var/run/mysqld directories to expense user.
COPY scripts/*.sql  /docker-entrypoint-initdb.d/
# till this command root access is available.

# USER expense
# from this command expense user access works.