# README

This README would simply document how to use rails credentials:edit for config/database.yml

Things you may want to cover:

* Ruby version
  * 2.6.0

* Rails version
  * 6.0.2.1

* Configuration
  * https://github.com/charlietag/test_rails_credentials/compare/v0.1.0...v0.1.1

* Credentials edit
  * `EDITOR=vim bundle exec rails credentials:edit`

    ```bash
    # aws:
    #   access_key_id: 123
    #   secret_access_key: 345
    
    
    # Used as the base secret for all MessageVerifiers in Rails, including the one protecting cookies.
    secret_key_base: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
    
    development:
      db:
        user: {db_user}
        pass: {db_password}
    
    production:
      db:
        user: {db_user}
        pass: {db_password}
    ```

* Testing credentials config
  * `bundle exec rails db:create`
    * `Created database 'test_rails_credentials_development'`
    * `Created database 'test_rails_credentials_test'`
  * `RAILS_ENV=production bundle exec rails db:create`
    * `Created database 'test_rails_credentials_production'`
