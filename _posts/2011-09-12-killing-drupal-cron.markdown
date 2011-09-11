---
layout: blog-post
title: Killing a hung Drupal 6 cron
---

Sometimes you will have a Drupal cron process that is stuck and you need to get rid of it. The problem is that Drupal stores the process information in the database and won't allow you to run a new cron until it is cleared out.

Restart apache to make sure the process is gone

    sudo /etc/init.d/apache2 restart

Run the following mysql commands on the database

    DELETE FROM variable WHERE name="cron_semaphore";
    DELETE FROM variable WHERE name="cron_last";
