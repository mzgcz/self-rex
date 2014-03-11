# install rex
# sudo aptitude install libnet-ssh2-perl curl openssh-server
# curl -L get.rexify.org | perl - --sudo -n Rex

user 'my-name';
password 'my-password';
pass_auth;

group myserver => "127.0.0.1";

desc "Get the uptime of all server";
task "uptime", group => "myserver", sub {
  my $output = run "uptime";
  say $output;
};
