<script>
    import { supabase } from './supabaseClient';
  
    let data = [];
  
    async function fetchData() {
      const { data: items, error } = await supabase.from('your-table').select('*');
      if (!error && items) {
        data = items;
      }
    }
  
    fetchData();
  </script>
  